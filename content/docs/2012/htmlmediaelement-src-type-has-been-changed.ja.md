---
title: "`HTMLMediaElement.src` の種類が変更されました"
date: "2012-12-03T03:50:54-05:00"
categories: ["audio-video", "dom"]
tags: []
releases: ["17"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=792665"
      title: "Bug 792665 – Separate HTMLMediaElement.src from HTMLMediaElement.srcObject"
---
従来 [`HTMLMediaElement`](https://developer.mozilla.org/docs/DOM/HTMLMediaElement).`src` プロパティの値はメディアストリームのオブジェクトとなっていました。標準化にあたって、`src` プロパティはメディアの URL 文字列とし、オブジェクトは別途新たな `srcObject` プロパティに含めるという提案を Mozilla が行い、Firefox の実装はそれにそった形に変更されました。今のところ `srcObject` は接頭辞付きの `mozSrcObject` となっています。

**更新**: `mozSrcObject` プロパティは [Firefox 42](https://www.fxsitecompat.dev/ja/docs/2015/htmlmediaelement-srcobject-has-been-unprefixed/) で接頭辞が外れ、[Firefox 58](https://www.fxsitecompat.dev/ja/docs/2017/htmlmediaelement-mozsrcobject-has-been-removed/) で削除されました。
