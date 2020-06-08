---
title: "`XHR.onuploadprogress` has been removed"
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
The [`XMLHttpRequest.onuploadprogress`](https://developer.mozilla.org/docs/XPCOM_Interface_Reference/nsIJSXMLHttpRequest#Attributes) property has not been standardized, and since Firefox 14 it has been deprecated with [a warning in the Error Console](https://bugzilla.mozilla.org/show_bug.cgi?id=743666). It's no longer available in Firefox 17 and later.
