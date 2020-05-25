---
title: "`ethiopic-numeric` の接頭辞が外れました"
date: "2014-07-22T05:06:26-04:00"
categories: ["css"]
tags: []
releases: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=985825"
      title: "Bug 985825 – Unprefix -moz-ethiopic-numeric"
supported_tools:
  firefox_extension: true
---
[`list-style-type`](https://developer.mozilla.org/docs/Web/CSS/list-style-type) 用の値 `ethiopic-numeric` のスタイルが CSS3 Counter Styles 仕様で定義されたことから、接頭辞が外れました。接頭辞付き値の対応は今後いずれかの時点で廃止されます。
