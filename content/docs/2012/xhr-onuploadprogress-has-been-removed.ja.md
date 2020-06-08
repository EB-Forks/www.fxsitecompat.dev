---
title: "`XHR.onuploadprogress` が廃止されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["dom"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=761278"
      title: "Bug 761278 – Remove XHR.onuploadprogress"
supported_tools:
  firefox_extension: true
---
`XMLHttpRequest` の [`onuploadprogress`](https://developer.mozilla.org/docs/XPCOM_Interface_Reference/nsIJSXMLHttpRequest#Attributes) プロパティは標準化されず、Firefox 14 以降非推奨となり [エラーコンソールに警告が表示されていました](https://bugzilla.mozilla.org/show_bug.cgi?id=743666)。Firefox 17 以降では使用できません。
