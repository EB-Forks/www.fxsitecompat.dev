---
title: "`HTMLMediaElement.mozSrcObject` が削除されました"
date: "2017-10-24T15:57:00-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1183495"
      title: "Bug 1183495 - Remove mozSrcObject alias to srcObject soon"
aliases:
    - "/ja/docs/2015/htmlmediaelement-mozsrcobject-will-be-removed/"
supported_tools:
  firefox_extension: true
---
[Firefox 42](https://www.fxsitecompat.dev/ja/docs/2015/htmlmediaelement-srcobject-has-been-unprefixed/) 以降廃止予定となっていた [`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) インターフェイス上の接頭辞付き `mozSrcObject` プロパティは Firefox 58 で削除されました。標準の [`srcObject`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/srcObject) プロパティで代用してください。
