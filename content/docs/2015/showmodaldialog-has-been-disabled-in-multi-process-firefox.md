---
title: "`showModalDialog()` has been disabled in multi-process Firefox"
date: "2015-12-29T21:46:00-05:00"
categories: ["dom"]
tags: []
releases: ["46", "52-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1077002"
      title: "Bug 1077002 - window.showmodaldialog does not work with e10s"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1234700"
      title: "Bug 1234700 - Hide window.showModalDialog, at least when e10s is enabled"
---
The [`window.showModalDialog`](https://developer.mozilla.org/docs/Web/API/Window/showModalDialog) method has been unavailable when Firefox is running in the multi-process mode codenamed [Electrolysis](https://wiki.mozilla.org/Electrolysis) (*e10s*). At least *Office 365* and *Exchange 2016* were known to be broken due to an exception thrown by Firefox.

Because it's technically difficult to support the functionality in *e10s* and the method has already been [deprecated since Firefox 28](https://www.fxsitecompat.dev/en-CA/docs/2013/showmodaldialog-has-been-deprecated/), Firefox 46 hid `showModalDialog` from `window` rather than fixing the error. *Office 365* and *Exchange 2016* are now working again thanks to their feature detection.

Currently, *e10s* is enabled by default only on Firefox Nightly and [Developer Edition](https://www.fxsitecompat.dev/en-CA/docs/2015/multi-process-is-enabled-by-default-on-the-developer-edition/). Once *e10s* is enabled on all Firefox channels in mid-2016, the method will [no longer be available](https://www.fxsitecompat.dev/en-CA/docs/2015/window-showmodaldialog-will-be-removed/) in Firefox.

**Update**: The method is no longer available on [Firefox 48](https://www.fxsitecompat.dev/en-CA/docs/2016/window-showmodaldialog-has-been-removed/) and later as *e10s* has been enabled by default.
