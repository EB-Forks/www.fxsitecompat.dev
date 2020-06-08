---
title: "`initCloseEvent()` と `createEvent(\'CloseEvent\')` が削除されました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1161950"
      title: "Bug 1161950 - Remove support for createEvent(\"CloseEvent\") / initCloseEvent"
supported_tools:
  firefox_extension: true
---
`CloseEvent.initCloseEvent` メソッドが削除され、[`document.createEvent`](https://developer.mozilla.org/docs/Web/API/Document/createEvent) メソッドでも `CloseEvent` タイプへの対応が打ち切られました。今後は代わりに [`CloseEvent`](https://developer.mozilla.org/docs/Web/API/CloseEvent/CloseEvent) コンストラクターを使ってください。
