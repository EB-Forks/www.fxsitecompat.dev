---
title: "`box-sizing` has been unprefixed"
date: "2014-02-07T11:57:09-05:00"
categories: ["css"]
tags: []
releases: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=243412"
      title: "Bug 243412 – Implement \'box-sizing\' (dropping the -moz- prefix)"
supported_tools:
  firefox_extension: true
---
The [`box-sizing`](https://developer.mozilla.org/docs/Web/CSS/box-sizing) property has been unprefixed. While `-moz-box-sizing` will be left for a reasonable period of time, developers are encouraged to use the unprefixed property instead.
