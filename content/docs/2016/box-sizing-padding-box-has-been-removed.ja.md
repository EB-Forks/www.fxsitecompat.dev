---
title: "`box-sizing:padding-box` が削除されました"
date: "2016-06-19T11:57:00-04:00"
categories: ["css"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1166728"
      title: "Bug 1166728 - remove box-sizing: padding-box"
aliases:
    - "/ja/docs/2015/box-sizing-padding-box-will-be-removed/"
supported_tools:
  firefox_extension: true
---
[`box-sizing`](https://developer.mozilla.org/docs/Web/CSS/box-sizing) CSS プロパティが `padding-box` を受け付けなくなりました。この値が仕様から削除されたためです。代わりに `border-box` を使ってください。
