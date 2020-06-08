---
title: "`mozallowfullscreen` has been unprefixed"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom", "html"]
tags: []
releases: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=805301"
      title: "Bug 805301 – Rename mozallowfullscreen to allowfullscreen"
---
The `mozallowfullscreen` attribute, that allows content in inline frames ([`<iframe>`](https://developer.mozilla.org/docs/Web/HTML/Element/iframe)) to be [fullscreen](https://developer.mozilla.org/docs/Web/Guide/DOM/Using_full_screen_mode), has been unprefixed. The corresponding `mozAllowFullScreen` property on the `HTMLIFrameElement` DOM interface has also been changed to `allowfullscreen`. The HTML5 `allowfullscreen` attribute is actually used for *YouTube*'s embedded players.
