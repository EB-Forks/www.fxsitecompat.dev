---
title: "`requestAnimationFrame()` in non-visible iframes is now throttled"
date: "2015-08-19T17:11:16-04:00"
categories: ["html"]
tags: []
releases: ["40", "45-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1145439"
      title: "Bug 1145439 - Throttle off-screen iframes to be more efficient"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1195592"
      title: "Bug 1195592 - FF 40.0.2: Disqus comments take much longer to load than prev version."
---
In order to improve performance and battery life, [`requestAnimationFrame`](https://developer.mozilla.org/docs/Web/API/Window/requestAnimationFrame) in [`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe)s that are not visible on the page is now throttled down, as if those are in background tabs. *Disqus* has had to fix an issue that took much longer to load comments because of hidden iframes with `requestAnimationFrame`.
