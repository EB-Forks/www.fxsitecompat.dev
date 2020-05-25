---
title: "Several internal CSS properties have been removed"
date: "2015-10-07T01:49:00-04:00"
categories: ["css"]
tags: []
releases: ["44", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1207002"
      title: "Bug 1207002 - Restrict MathML-related internal properties to only be accessible in UA sheets"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1211040"
      title: "Bug 1211040 - Restrict -moz-window-{dragging, shadow} to chrome only"
supported_tools:
  firefox_extension: true
---
Some internal CSS properties for [MathML](https://developer.mozilla.org/docs/Web/MathML) and browser theming, including `-moz-math-display`, `-moz-window-dragging` and [`-moz-window-shadow`](https://developer.mozilla.org/docs/Web/CSS/-moz-window-shadow), are no longer available from Web content.

**Update**: The `-moz-window-dragging` property has been [restored](https://bugzilla.mozilla.org/show_bug.cgi?id=1212607) due to a compatibility issue with the *Graphene* runtime.
