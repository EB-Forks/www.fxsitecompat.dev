---
title: "`Navigator.requestWakeLock()` has been disabled except on Firefox OS"
date: "2014-03-21T04:50:04-04:00"
categories: ["dom"]
tags: []
releases: ["30", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=963366"
      title: "Bug 963366 – Hide navigator.requestWakeLock and MozWakeLock from the web except on Firefox OS"
supported_tools:
  firefox_extension: true
---
The [`Navigator.requestWakeLock`](https://developer.mozilla.org/docs/Web/API/Navigator.requestWakeLock) method and the [`MozWakeLock`](https://developer.mozilla.org/docs/Web/API/MozWakeLock) object, a part of the [Power Management API](https://developer.mozilla.org/docs/WebAPI/Power_Management), are useful only on Firefox OS but have been exposed to all platforms. Those are no longer available except on Firefox OS.
