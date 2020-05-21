---
title: "`Array.keys()` and `Array.entries()` have been implemented"
date: "2013-12-09T02:32:17-05:00"
categories: ["javascript"]
tags: []
releases: ["28", "31-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=894658"
      title: "Bug 894658 – Implement ES6 Array.prototype.{keys, entries}"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=958095"
      title: "Bug 958095 – Array.prototype.keys() breaks web apps, e.g. dagre-d3"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=987762"
      title: "Bug 987762 – Firefox 28.0 javascript xhr raw response object (from json API) has a property \'entries\' which is a [native code] function"
---
As part of [ECMAScript 6 support](https://developer.mozilla.org/docs/Web/JavaScript/ECMAScript_6_support_in_Mozilla), the [`Array.keys`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/keys) and [`Array.entries`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/entries) methods have been added. This may break some JavaScript libraries which are extending [`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) with their own methods. Regressions have been found at least in 2 apps, and the *dagre-d3* JavaScript library affecting one of them was fixed during the Aurora development cycle.
