---
title: "`:any-link` CSS 擬似クラスの接頭辞が外れました"
date: "2016-07-26T12:42:00-04:00"
categories: ["css"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=843579"
      title: "Bug 843579 - Remove prefix from :any-link"
supported_tools:
  firefox_extension: true
---
The [`:any-link`](https://developer.mozilla.org/docs/Web/CSS/:any-link) CSS4 擬似クラスがベンダー接頭辞なしに Firefox で使用可能となりました。接頭辞付きの `:-moz-any-link` 擬似クラスへの対応は近い将来削除されます。
