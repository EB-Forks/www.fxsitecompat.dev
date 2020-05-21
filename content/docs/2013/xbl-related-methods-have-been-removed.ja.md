---
title: "XBL 関連のメソッドが削除されました"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
releases: ["26", "31-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=912322"
      title: "Bug 912322 – document.getAnonymous* should not be available to web content"
---
[XBL DOM インターフェイス](https://developer.mozilla.org/docs/XBL/XBL_1.0_Reference/DOM_Interfaces) 上に実装されている次のメソッドが [`Document`](https://developer.mozilla.org/docs/Web/API/Document) から削除されました。`getAnonymousNodes`、`getAnonymousElementByAttribute`、`getBindingParent`、`loadBindingDocument`
