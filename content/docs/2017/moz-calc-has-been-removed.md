---
title: "`-moz-calc()` has been removed"
date: "2017-01-18T10:27:00-05:00"
categories: ["css"]
tags: []
releases: ["53", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1331296"
      title: "Bug 1331296 - Remove support for -moz-calc()"
supported_tools:
  firefox_extension: true
---
The support for the prefixed `-moz-calc` CSS function has been removed with Firefox 53 in favour of the standard, unprefixed [`calc`](https://developer.mozilla.org/docs/Web/CSS/calc) function available since [Firefox 16](https://www.fxsitecompat.dev/en-CA/docs/2012/various-css-properties-have-been-unprefixed/).
