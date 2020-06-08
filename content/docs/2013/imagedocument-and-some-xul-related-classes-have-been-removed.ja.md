---
title: "`ImageDocument` と一部の XUL 関連クラスが削除されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
releases: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885177"
      title: "Bug 885177 – Make window.ImageDocument ChromeOnly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=898687"
      title: "Bug 898687 – Remove XULTreeBuilder from content"
supported_tools:
  firefox_extension: true
---
非標準の `ImageDocument` インターフェイスと、`BoxObject`、`TreeColumn`、`TreeColumns`、`TreeContentView`、`TreeSelection`、`XULControllers`、`XULTemplateBuilder`、`XULTreeBuilder` インターフェイスが、ウェブコンテンツから使用できなくなりました。
