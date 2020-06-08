---
title: "`XMLHttpRequest.mozBackgroundRequest` has been removed"
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
The non-standard `mozBackgroundRequest` property on the [`XMLHttpRequest`](https://developer.mozilla.org/docs/Web/API/XMLHttpRequest) interface is no longer available from Web content.
