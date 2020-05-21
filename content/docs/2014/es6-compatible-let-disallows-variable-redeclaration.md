---
title: "ES6-compatible `let` disallows variable redeclaration"
date: "2014-10-17T22:50:44-04:00"
categories: ["javascript"]
tags: []
releases: ["35", "38-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1001090"
      title: "Bug 1001090 – Implement ES6 \"temporal dead zone\" for let"
---
The [`let`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let) statement implementation has been updated to support the "[temporal dead zone](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Statements/let#Temporal_dead_zone_and_errors_with_let)" of the ECMAScript 6 spec, though the implementation is not yet fully ES6-compatible. Starting with Firefox 35, redeclaring an existing variable in the same block scope throws a [`TypeError`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/TypeError), while referring a variable before the variable is declared raises a [`ReferenceError`](https://developer.mozilla.org/docs/JavaScript/Reference/Global_Objects/ReferenceError). This change will mainly affect [Open Web Apps](https://developer.mozilla.org/Apps) for Firefox and Firefox OS, as well as [Firefox extensions](https://developer.mozilla.org/Add-ons). See also the [newsgroup announcement](https://groups.google.com/d/topic/mozilla.dev.platform/tezdW299Zds/discussion) for details.

**Update**: Starting with Firefox 46, redeclaration of variables will [throw a `SyntaxError`](https://bugzilla.mozilla.org/show_bug.cgi?id=1198833) instead of `TypeError` as per the spec.
