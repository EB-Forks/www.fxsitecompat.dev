---
title: "`DocumentTouch` has been removed"
date: "2013-07-14T19:12:37-04:00"
categories: ["dom"]
tags: []
releases: ["25", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=897211"
      title: "Bug 897211 – Remove nsIDOMDocumentTouch"
supported_tools:
  firefox_extension: true
---
The [`DocumentTouch`](https://developer.mozilla.org/docs/Web/API/DocumentTouch) interface has been removed due to the removal from the spec. The [`createTouch`](https://developer.mozilla.org/docs/Web/API/DocumentTouch.createTouch) and [`createTouchList`](https://developer.mozilla.org/docs/Web/API/DocumentTouch.createTouchList) methods have been moved to the [`Document`](https://developer.mozilla.org/docs/Web/API/Document) interface.
