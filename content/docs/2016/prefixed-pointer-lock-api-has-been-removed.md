---
title: "Prefixed Pointer Lock API has been removed"
date: "2016-07-31T17:13:00-04:00"
categories: ["dom"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=991899"
      title: "Bug 991899 - Unprefix pointer lock"
---
The [Pointer Lock API](https://developer.mozilla.org/docs/Web/API/Pointer_Lock_API) has been unprefixed as the spec is now considered stable. This includes the [`Document.pointerLockElement`](https://developer.mozilla.org/docs/Web/API/Document/pointerLockElement) property, the [`Element.requestPointerLock`](https://developer.mozilla.org/docs/Web/API/Element/requestPointerLock) and [`Document.exitPointerLock`](https://developer.mozilla.org/docs/Web/API/Document/exitPointerLock) methods, as well as the [`pointerlockchange`](https://developer.mozilla.org/docs/Web/Events/pointerlockchange) and [`pointerlockerror`](https://developer.mozilla.org/docs/Web/Events/pointerlockerror) events.

At the same time, the `moz`-prefixed API is disabled by default without a transition period. Besides, the `mozMovementX` and `mozMovementY` properties on the `MouseEvent` interface, deprecated since [Firefox 41](https://www.fxsitecompat.dev/en-CA/docs/2015/mouseevent-movementxy-have-been-unprefixed/), have also been disabled. Given that Google Chrome has already removed the `webkit`-prefixed API support, Mozilla developers are not expecting any compatibility issues.
