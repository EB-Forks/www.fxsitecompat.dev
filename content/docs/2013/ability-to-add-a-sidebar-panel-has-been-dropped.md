---
title: "Ability to add a sidebar panel has been dropped"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
releases: ["23", "24-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691647"
      title: "Bug 691647 – clean up nsISidebar (remove window.sidebar.addPanel/addPersistentPanel)"
---
`window.sidebar.addPanel` and `window.sidebar.addPersistentPanel` are no longer supported. These methods were a part of a Netscape-derived API which allowed Web publishers to integrate their contents as sidebar panels of the browser. They were not standardized, rarely used, and not very well supported. No other browsers have implemented these.

There is also a [plan](https://www.fxsitecompat.dev/en-CA/docs/2015/window-sidebar-will-be-removed/) to remove [`window.sidebar`](https://developer.mozilla.org/docs/Web/API/window.sidebar) itself in the future.

As alternatives to those API, you can [create a sidebar extension or utilize the Social API](https://developer.mozilla.org/docs/Creating_a_Firefox_sidebar).
