---
title: "`Element.mozMatchesSelector()` will be removed"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119718"
      title: "Bug 1119718 - Remove mozMatchesSelector"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1216193"
      title: "Bug 1216193 - Implement webkitMatchesSelector"
supported_tools:
  firefox_extension: true
---
The `Element.mozMatchesSelector` method will be removed in the future in favour of the standard [`Element.matches`](https://developer.mozilla.org/docs/Web/API/Element/matches) method available since [Firefox 34](https://www.fxsitecompat.dev/en-CA/docs/2014/element-matches-has-been-unprefixed/). Firefox 44 has also implemented `webkitMatchesSelector` which is now standardized for Web interoperability, though the unprefixed method is always preferred.
