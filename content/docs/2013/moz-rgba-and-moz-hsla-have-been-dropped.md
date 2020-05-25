---
title: "`-moz-rgba()` and `-moz-hsla()` have been dropped"
date: "2013-10-08T20:15:35-04:00"
categories: ["css"]
tags: []
releases: ["27", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=893319"
      title: "Bug 893319 – remove -moz-rgba() and -moz-hsla()"
supported_tools:
  firefox_extension: true
---
The support of the prefixed `-moz-rgba()` and `-moz-hsla()` functional notations for [colour values](https://developer.mozilla.org/docs/Web/CSS/color_value) has been removed. The standard, unprefixed `rgba()` and `hsla()` notations should be used instead.
