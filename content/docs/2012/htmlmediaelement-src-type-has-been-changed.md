---
title: "`HTMLMediaElement.src` type has been changed"
date: "2012-12-03T03:50:54-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=792665"
      title: "Bug 792665 – Separate HTMLMediaElement.src from HTMLMediaElement.srcObject"
---
Previously the value of the [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement).`src` property was a media stream object. In the process of standardization, Mozilla has proposed that the `src` property represents a URL string of the media while the new `srcObject` property has the object. The Firefox implementation has been changed to reflect the proposal. For now, `srcObject` is prefixed `mozSrcObject`.

**Update**: The `mozSrcObject` property has been unprefixed with [Firefox 42](https://www.fxsitecompat.dev/en-CA/docs/2015/htmlmediaelement-srcobject-has-been-unprefixed/) and removed with [Firefox 58](https://www.fxsitecompat.dev/en-CA/docs/2017/htmlmediaelement-mozsrcobject-has-been-removed/).
