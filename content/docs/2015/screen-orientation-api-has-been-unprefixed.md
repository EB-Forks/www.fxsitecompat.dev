---
title: "Screen Orientation API has been unprefixed"
date: "2015-09-09T17:20:00-04:00"
categories: ["dom"]
tags: []
releases: ["43", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1131470"
      title: "Bug 1131470 - w3c screen orientation api has changed"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/zyGP6PemJlg/discussion"
      title: "Intent to Ship: Screen Orientation API"
supported_tools:
  firefox_extension: true
---
Firefox 43 has implemented the latest standard [Screen Orientation API](https://w3c.github.io/screen-orientation/) that offers the `type`, `angle` and `onchange` properties as well as the `lock` and `unlock` methods on `window.screen.orientation`.

The experimental, prefixed implementation available since Firefox 14, including the `mozOrientation` and `onmozorientationchange` properties as well as the `mozLockOrientation` and `mozUnlockOrientation` methods on [`window.screen`](https://developer.mozilla.org/docs/Web/API/Screen), will be removed in the future.
