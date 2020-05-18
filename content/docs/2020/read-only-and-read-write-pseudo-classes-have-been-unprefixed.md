---
title: "`:read-only` and `:read-write` pseudo-classes have been unprefixed"
date: "2020-05-15T21:23:00-04:00"
categories: ["css"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=312971"
      title: "Bug 312971 - Support :read-only and :read-write pseudoclasses (unprefix)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=888884"
      title: "Bug 888884 - :-moz-read-write pseudo-class shouldn't be applied on <input type=text disabled> and <textarea disabled>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3CguC7Mp3yQ/discussion"
      title: "Intent to ship: :read-only / :read-write pseudo-classes"
supported_tools:
  firefox_extension: true
---
The [`:read-only`](https://developer.mozilla.org/docs/Web/CSS/:read-only) and [`:read-write`](https://developer.mozilla.org/docs/Web/CSS/:read-write) CSS pseudo-classes have become available in Firefox 78 and later. The prefixed `:-moz-read-only` and `:-moz-read-write` pseudo-classes remain as the aliases, but the support will be removed in the future.

Firefox 78 has also fixed a standard-compliant issue of `:read-write` so that it will no longer be applied to disabled `<input>` and `<textarea>` elements, according the [HTML spec](https://html.spec.whatwg.org/#selector-read-write).
