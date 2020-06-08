---
title: "`window.external.AddSearchProvider()` がダミー関数となりました"
date: "2020-05-23T18:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632447"
      title: "Bug 1632447 - Disable window.{external|sidebar}.AddSearchProvider by preference"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vSV-gg5621k/discussion"
      title: "Intent to unship: window.external.AddSearchProvider"
supported_tools:
  firefox_extension: true
---
Firefox 78 以降、`window.external.AddSearchProvider` とそのエイリアスである `window.sidebar.AddSearchProvider` は、[HTML 仕様](https://html.spec.whatwg.org/multipage/obsolete.html#external) に従い、何もしないダミー関数となります。この Internet Explorer 由来の旧式メソッドは [Firefox 65](https://www.fxsitecompat.dev/ja/docs/2018/window-sidebar-and-window-external-addsearchprovider-have-been-deprecated/) 以降廃止予定となっていました。Google は 2016 年に [Chrome 54](https://www.chromestatus.com/feature/5672001305837568) で既にこれをダミー関数としており、他のモダンブラウザーは非対応です。

あなたのウェブサイトで独自の検索プロバイダーを提供したい場合は、まだ 2 つの方法があります。

* `<link rel="search">` を使って、あなたのサイト上で [検索プロバイダー自動検出](https://developer.mozilla.org/docs/Web/OpenSearch#Autodiscovery_of_search_plugins) に対応する
* [`chrome_settings_overrides`](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/chrome_settings_overrides) マニフェストキーを使って、検索プロバイダーを追加するブラウザー拡張機能を作成する

Netscape 由来の非標準 `window.sidebar` オブジェクトは [近い将来削除されます](https://www.fxsitecompat.dev/ja/docs/2015/window-sidebar-will-be-removed/)。
