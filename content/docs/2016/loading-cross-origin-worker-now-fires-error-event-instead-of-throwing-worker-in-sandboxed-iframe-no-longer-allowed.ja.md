---
title: "クロスオリジンの Worker 読み込みが例外の代わりに `error` イベントを発生させるようになり、サンドボックス化された iframe 内の Worker が禁止されます"
date: "2016-04-02T01:39:00-04:00"
categories: ["dom", "privacy-security"]
tags: []
releases: ["45", "45-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1218433"
      title: "Bug 1218433 - Use AsyncOpen2 in dom/workers/ScriptLoader.cpp"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1241888"
      title: "Bug 1241888 - Loading cross-origin worker scripts does not throw a SecurityError"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260388"
      title: "Bug 1260388 - Web worker fails to load in sandboxed iframe with Firefox 45"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1260961"
      title: "Bug 1260961 - PDF.js doesn't work with cross-origin environment, because worker no longer throws on Firefox 45+ and onerror handler is missing"
aliases:
    - "/ja/docs/2016/loading-cross-origin-worker-no-longer-throws-worker-in-sandboxed-iframe-will-fail/"
---
HTML5 標準準拠の一環として、Firefox 45 で [Web Worker](https://developer.mozilla.org/docs/Web/API/Web_Workers_API) スクリプトを内部的に読み込む方法が変更されました。ここで知っておくべき後方互換性問題が 2 件あります。

従来、[`Worker`](https://developer.mozilla.org/docs/Web/API/Worker/Worker) コンストラクターでクロスオリジンの Worker スクリプトを読み込もうとした場合、Firefox は即座に `SecurityError` を投げていました。Firefox 45 以降では、最新の仕様に従い、新しい `Worker` インスタンスが作成された後に非同期で一般的な `error` イベントが発生します。両方の場合に対処するには、以下のように [`try-catch`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/try...catch) 宣言と Worker の [`onerror`](https://developer.mozilla.org/docs/Web/API/AbstractWorker/onerror) ハンドラーを併用しなければなりません。

```js
try {
  var worker = new Worker(url);
  worker.addEventListener('error', function (event) {
    // Error: Failed to load script (nsresult = 0x805303f4)
    // イベントの浮上を防ぐ
    event.preventDefault();
    // 新しいブラウザー向けにクロスオリジン読み込みエラーを処理
    ...
  });
} catch (ex) {
  // SecurityError
  // 古いブラウザー向けにクロスオリジン読み込みエラーを処理
  ...
}
```
現在のところ Mozilla の [*PDF.js*](https://mozilla.github.io/pdf.js/) ライブラリが CDN などのクロスオリジン環境で動作していません。これは、Worker に `onerror` ハンドラーが欠けており、フォールバック関数が呼び出されないためです。

**更新**: *PDF.js* バージョン 1.4.187 で問題が修正されました。[pdf.js レポジトリ](https://github.com/mozilla/pdf.js/releases) で新バージョンが公開されるまでは、最新のプレビルド版を [pdfjs-dist レポジトリ](https://github.com/mozilla/pdfjs-dist) からダウンロードできます。自分でビルドすることも可能です。

Firefox 45 では、`sandbox` 属性付き [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe) 内で Worker の読み込みが誤って許容されているというブラウザー実装上のバグも修正されました。サンドボックス化された iframe 内のドキュメントは何にも一致しない独自のオリジンを持つ一方で、Worker スクリプトは [同一オリジン](https://developer.mozilla.org/docs/Web/Security/Same-origin_policy) になければならないため、今後そうしたコードは上記のようにエラーとなります。この問題の回避策は `sandbox` の値に `allow-same-origin` を追加することですが、保護機能が緩和されてしまうことから推奨されません。
