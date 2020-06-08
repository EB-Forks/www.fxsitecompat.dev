---
title: "`mozIndexedDB` が削除されました"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
releases: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=975699"
      title: "Bug 975699 – Remove mozIndexedDB again"
supported_tools:
  firefox_extension: true
---
[Firefox 16](https://www.fxsitecompat.dev/ja/docs/2012/several-apis-have-been-unprefixed/) で接頭辞が外れたものの [互換性](https://bugzilla.mozilla.org/show_bug.cgi?id=770844) のために残されていた `mozIndexedDB` オブジェクトがついに `window` から削除されました。今後は標準の [`indexedDB`](https://developer.mozilla.org/docs/Web/API/IDBEnvironment/indexedDB) プロパティを使用してください。
