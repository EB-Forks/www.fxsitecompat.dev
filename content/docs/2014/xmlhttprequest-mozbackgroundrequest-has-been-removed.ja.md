---
title: "`XMLHttpRequest.mozBackgroundRequest` が削除されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
releases: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035242"
      title: "Bug 1035242 – Make XMLHttpRequest.mozBackgroundRequest chrome-only"
supported_tools:
  firefox_extension: true
---
[`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) インターフェイス上の非標準プロパティ `mozBackgroundRequest` はウェブコンテンツから使用できなくなりました。
