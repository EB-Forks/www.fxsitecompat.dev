---
title: "`mozIndexedDB` has been removed"
date: "2015-02-27T04:21:22-05:00"
categories: ["dom"]
tags: []
releases: ["38", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=975699"
      title: "Bug 975699 – Remove mozIndexedDB again"
---
The `mozIndexedDB` object, unprefixed with [Firefox 16](https://www.fxsitecompat.dev/en-CA/docs/2012/several-apis-have-been-unprefixed/) but preserved for a [compatibility reason](https://bugzilla.mozilla.org/show_bug.cgi?id=770844), has finally been removed from `window` in favour of the standard [`indexedDB`](https://developer.mozilla.org/docs/Web/API/IDBEnvironment/indexedDB) property.
