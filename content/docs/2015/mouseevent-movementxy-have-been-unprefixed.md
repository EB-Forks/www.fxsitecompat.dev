---
title: "`MouseEvent.movementX`/`Y` have been unprefixed"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1164981"
      title: "Bug 1164981 - Add MouseEvent.movementX/Y"
---
The [`MouseEvent.movementX`](https://developer.mozilla.org/docs/Web/API/MouseEvent/movementX) and [`MouseEvent.movementY`](https://developer.mozilla.org/docs/Web/API/MouseEvent/movementY) properties have been unprefixed. The `moz`-prefixed properties will be removed in the future.

**Update**: These properties have been removed with [Firefox 50](https://www.fxsitecompat.dev/en-CA/docs/2016/prefixed-pointer-lock-api-has-been-removed/).
