---
title: "`target=_blank` on anchors now implies `rel=noopener`"
date: "2020-06-07T22:43:00-04:00"
categories: ["dom", "html", "privacy-security"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503681"
      title: "Bug 1503681 - Make target=_blank on anchors imply rel=noopener"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1522083"
      title: "Bug 1522083 - Make target=_blank on a/area elements imply rel=noopener by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DDQP5xIKYiY/discussion"
      title: "Intent to ship: implicit ref=noopener for target=_blank on anchor and area elements"
supported_tools:
  firefox_extension: true
---
Starting with Firefox 79, `<a>` and `<area>` elements having `target="_blank"` will imply `rel="noopener"` if no `rel` attribute is set on the element, according to the [current HTML spec](https://github.com/whatwg/html/issues/4078). The [`noopener`](https://developer.mozilla.org/docs/Web/HTML/Link_types/noopener) link type makes [`window.opener`](https://developer.mozilla.org/docs/Web/API/Window/opener) `null` in the new window, preventing the DOM property from being abused by untrusted third-party sites. If needed, explicitly setting `rel="opener"` reverses the course.

Apple made the change first with [Safari 12.1](https://developer.apple.com/documentation/safari_release_notes/safari_12_1_release_notes) shipped in March 2019. In Firefox, the new behaviour has been enabled by default in the Nightly and early Beta channels since Firefox 65. [Google Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=898942) may also follow.
