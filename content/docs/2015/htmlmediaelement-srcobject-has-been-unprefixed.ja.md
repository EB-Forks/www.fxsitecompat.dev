---
title: "`HTMLMediaElement.srcObject` の接頭辞が外れました"
date: "2015-08-05T00:48:18-04:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["42", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1175523"
      title: "Bug 1175523 - Unprefix mozSrcObject (to srcObject)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1183495"
      title: "Bug 1183495 - Remove mozSrcObject alias to srcObject soon"
---
[`HTMLMediaElement`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement) インターフェイス上の [`srcObject`](https://developer.mozilla.org/docs/Web/API/HTMLMediaElement/srcObject) プロパティの接頭辞が外れました。接頭辞付き `mozSrcObject` プロパティはエイリアスとして残されていますが、近々削除されます。

**更新**: `mozSrcObject` プロパティは [Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/htmlmediaelement-mozsrcobject-has-been-removed/) で削除されました。
