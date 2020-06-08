---
title: "`WindowUtils` が削除されました"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
releases: ["32", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1017820"
      title: "Bug 1017820 – Remove the classinfo for DOMWindowUtils"
supported_tools:
  firefox_extension: true
---
グローバルオブジェクトを標準化する現在進行中の取り組みの一環として、[`window`](https://developer.mozilla.org/docs/Web/API/window) から非標準の `WindowUtils` インターフェイスが削除されました。
