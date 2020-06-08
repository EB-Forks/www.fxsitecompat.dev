---
title: "`window.content` will be removed"
date: "2017-09-13T07:19:00-04:00"
categories: ["dom"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=864845"
      title: "Bug 864845 - Make window.content chrome-only in nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1400140"
      title: "Bug 1400140 - Make window.content chrome-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632143"
      title: "Bug 1632143 - Make window.content chrome-only in early betas"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Tmbs-wFwHzo/discussion"
      title: "Intent to unship: Visibility of window.content to untrusted code"
aliases:
    - "/en-CA/docs/2017/window-content-has-been-removed/"
supported_tools:
  firefox_extension: true
---
The non-standard [`window.content`](https://developer.mozilla.org/docs/Web/API/Window/content) object is no longer available from web content on Firefox Nightly 57 and later. It will be removed from other channels as well once [Telemetry](https://telemetry.mozilla.org/) proves low usage.

This object isn't useful because it's just an alias of [`window.top`](https://developer.mozilla.org/docs/Web/API/Window/top) or simply [`window`](https://developer.mozilla.org/docs/Web/API/Window) in many cases, but it may have been misused for browser detection purposes on the web, like [`window.controllers`](https://developer.mozilla.org/docs/Web/API/Window/controllers) that was once removed with [Firefox 29](https://www.fxsitecompat.dev/en-CA/docs/2014/window-content-controllers-pkcs11-and-loadstatus-have-been-removed/) but added back to retain backward compatibility. Web developers should always avoid using these kind of non-standard features.

**Update**: Starting with Firefox 77, `window.content` is disabled on the early Beta channel as well.
