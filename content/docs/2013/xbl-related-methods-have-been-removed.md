---
title: "XBL-related methods have been removed"
date: "2013-09-19T23:58:13-04:00"
categories: ["dom"]
tags: []
releases: ["26", "31-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=912322"
      title: "Bug 912322 – document.getAnonymous* should not be available to web content"
---
The following methods implemented on the [XBL DOM interface](https://developer.mozilla.org/docs/XBL/XBL_1.0_Reference/DOM_Interfaces) have been removed from the [`Document`](https://developer.mozilla.org/docs/Web/API/Document) interface: `getAnonymousNodes`, `getAnonymousElementByAttribute`, `getBindingParent`, and `loadBindingDocument`.
