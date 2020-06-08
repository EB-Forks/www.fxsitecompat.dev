---
title: "Several APIs have been unprefixed"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=726378"
      title: "Bug 726378 – Unprefix IndexedDB"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=769571"
      title: "Bug 769571 – Unprefix battery and vibrator APIs"
supported_tools:
  firefox_extension: true
---
The [IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API) API has been unprefixed. Now you can use the standard [`indexedDB`](https://developer.mozilla.org/docs/Web/API/IDBEnvironment/indexedDB) object instead of `mozIndexedDB`.

The [Battery Status](https://developer.mozilla.org/docs/Web/API/Battery_Status_API) and [Vibration](https://developer.mozilla.org/docs/Web/API/Vibration_API) APIs have also been unprefixed. The prefixed `navigator.mozBattery` and `navigator.mozVibrate` methods are no longer available.

**Update**: The `mozIndexedDB` object has been removed with [Firefox 38](https://www.fxsitecompat.dev/en-CA/docs/2015/mozindexeddb-has-been-removed/).

**Update 2**: The Battery Status API has been removed with [Firefox 52](https://www.fxsitecompat.dev/en-CA/docs/2016/battery-status-api-has-been-removed/).
