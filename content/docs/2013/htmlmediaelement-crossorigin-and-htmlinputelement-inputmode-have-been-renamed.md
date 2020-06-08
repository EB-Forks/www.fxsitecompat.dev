---
title: "`HTMLMediaElement.crossorigin` and `HTMLInputElement.inputmode` have been renamed"
date: "2013-02-24T03:44:31-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=847370"
      title: "Bug 847370 – HTMLMediaElement - crossOrigin vs crossorigin"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=850346"
      title: "Bug 850346 – inputmode vs inputMode for nsHTMLInputElement"
supported_tools:
  firefox_extension: true
---
[`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement)'s `crossorigin` property has been renamed to `crossOrigin`, and [`HTMLInputElement`](https://developer.mozilla.org/docs/Web/API/HTMLInputElement)'s `inputmode` property has also been renamed to `inputMode` to comply with the spec (note the capital letters).
