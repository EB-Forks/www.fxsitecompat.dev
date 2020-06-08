---
title: "`window.openDialog()` has been removed"
date: "2014-06-09T02:46:54-04:00"
categories: ["dom"]
tags: []
releases: ["32", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=962747"
      title: "Bug 962747 – Hide Window.openDialog from content"
supported_tools:
  firefox_extension: true
---
The non-standard [`window.openDialog`](https://developer.mozilla.org/docs/Web/API/window.openDialog) method is no longer available from Web content. [`window.open`](https://developer.mozilla.org/docs/Web/API/window.open) should be used instead.
