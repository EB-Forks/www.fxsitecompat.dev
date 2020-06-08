---
title: "`URL.createObjectURL()` が `MediaStream` を引数として受け付けなくなりました"
date: "2018-04-24T19:23:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["62", "68-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1454889"
      title: "Bug 1454889 - Remove createObjectURL()'s MediaStream overload"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1483220"
      title: "Bug 1483220 - Camera not found trying to stream on Facebook"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/o_0RoYoCmM4/discussion"
      title: "Intent to unship: URL.createObjectURL(MediaStream)"
supported_tools:
  firefox_extension: true
---
Firefox 62 以降、[`URL.createObjectURL`](https://developer.mozilla.org/docs/Web/API/URL/createObjectURL) 静的メソッドは [`MediaStream`](https://developer.mozilla.org/docs/Web/API/MediaStream) オブジェクトを引数として受け付けなくなりました。現在の仕様によれば、`Blob` あるいは `MediaSource` オブジェクトのみ受け付けられます。

ストリーム引数対応は [Firefox 54 以降廃止予定](https://www.fxsitecompat.dev/ja/docs/2017/url-createobjecturl-stream-has-been-deprecated/) とされていました。[Safari](https://bugs.webkit.org/show_bug.cgi?id=167518) は既にこの変更を行っており、[Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=800767) もすぐに後を追うことでしょう。

`<video>` あるいは `<audio>` 要素上に `MediaStream` オブジェクトを設定したい場合は、以下のように [`HTMLMediaElement.prototype.srcObject`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/srcObject) プロパティを使ってください。

```js
// これは動作しません
video.src = URL.createObjectURL(stream);
// このように書き換えてください
video.srcObject = stream;
```

**更新**: この変更によりデスクトップ上で *Facebook Live* が動作していません。
