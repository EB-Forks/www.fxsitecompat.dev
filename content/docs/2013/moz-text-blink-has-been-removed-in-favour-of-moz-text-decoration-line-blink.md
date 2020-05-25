---
title: "`-moz-text-blink` has been removed in favour of `-moz-text-decoration-line:blink`"
date: "2013-09-19T23:58:13-04:00"
categories: ["css"]
tags: []
releases: ["26", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=812995"
      title: "Bug 812995 – add \'blink\' to -moz-text-decoration-line and drop -moz-text-blink"
aliases:
    - "/en-CA/docs/2013/moz-text-blink-has-been-removed-in-favor-of-moz-text-decoration-line-blink/"
supported_tools:
  firefox_extension: true
---
The non-standard [`-moz-text-blink`](https://developer.mozilla.org/docs/Web/CSS/-moz-text-blink) property has been removed. Instead, the standard, still prefixed [`text-decoration-line`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-line) property now takes `blink` as a valid value. Actually it doesn't blink any content on Firefox though, from the perspective of [accessibility](https://developer.mozilla.org/docs/Accessibility). Note that the blink effect with `text-decoration:blink` has been [dropped with Firefox 23](https://www.fxsitecompat.dev/en-CA/docs/2013/blink-effect-with-text-decoration-blink-has-been-dropped/).
