---
title: "`:is()` pseudo-class has been unprefixed"
date: "2020-05-24T16:50:00-04:00"
categories: ["css"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1509418"
      title: "Bug 1509418 - Implement `:is()` and `:where()` selectors"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632646"
      title: "Bug 1632646 - Enable :is() / :where() on all release channels."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/_f8gYPevIQw/discussion"
      title: "Intent to prototype and ship: CSS :is() and :where() pseudo-classes."
supported_tools:
  firefox_extension: true
---
The [`:is()`](https://developer.mozilla.org/docs/Web/CSS/:is) and [`:where()`](https://developer.mozilla.org/docs/Web/CSS/:where) CSS pseudo-classes from the [Selectors Level 4 spec](https://drafts.csswg.org/selectors/) have been enabled with Firefox 78. In Firefox, `:is()` had been implemented as `:-moz-any()` for a long time. The prefixed pseudo-class is still available but may be removed in the future. Make sure to use both the standard and non-standard versions to future-proof your website.
