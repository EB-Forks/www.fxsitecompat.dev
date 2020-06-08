---
title: "`HTMLMediaElement.mozSrcObject` has been removed"
date: "2017-10-24T15:57:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1183495"
      title: "Bug 1183495 - Remove mozSrcObject alias to srcObject soon"
aliases:
    - "/en-CA/docs/2015/htmlmediaelement-mozsrcobject-will-be-removed/"
supported_tools:
  firefox_extension: true
---
The prefixed `mozSrcObject` property on the [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) interface, deprecated since [Firefox 42](https://www.fxsitecompat.dev/en-CA/docs/2015/htmlmediaelement-srcobject-has-been-unprefixed/), has been removed with Firefox 58. Use the standard [`srcObject`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/srcObject) property instead.
