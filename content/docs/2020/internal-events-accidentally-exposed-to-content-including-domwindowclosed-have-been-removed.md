---
title: "Internal events accidentally exposed to content, including `DOMWindowClosed`, have been removed"
date: "2020-06-03T00:47:00-04:00"
categories: ["dom"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557407"
      title: "Bug 1557407 - Don't expose the `DOMWindowClosed` event to content"
---
A Firefox developer noticed that more than a dozen of non-standard, internal events had been exposed to the web, mostly accidentally, but some were for testing purposes. As of Firefox 79, these events are no longer available to web content:

* `DOMWindowClose`: Fired when a new tab or popup window was about to be closed with `window.close()`
* `fullscreen`: Not to be confused with [`fullscreenchange`](https://developer.mozilla.org/docs/Web/API/Element/fullscreenchange_event)
* `MozBeforeInitialXULLayout`
* `MozMouseScrollFailed`
* `MozMouseScrollTransactionTimeout`
* `MozPaintWait`
* `MozPaintWaitFinished`
* `MozPerformDelayedBlur`
* `occlusionstatechange`
* `resolutionchange`
* `willenterfullscreen`
* `willexitfullscreen`
* `XULAlertClose`
