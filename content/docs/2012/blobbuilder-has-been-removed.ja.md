---
title: "`BlobBuilder` が廃止されました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
releases: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=744907"
      title: "Bug 744907 – Remove BlobBuilder"
supported_tools:
  firefox_extension: true
---
廃止予定となっていた [`BlobBuilder`](https://developer.mozilla.org/docs/DOM/BlobBuilder) (`MozBlobBuilder`) インターフェイスが削除されました。今後 `Blob` オブジェクトを作成するには [`Blob`](https://developer.mozilla.org/docs/DOM/Blob) コンストラクターを使用してください。
