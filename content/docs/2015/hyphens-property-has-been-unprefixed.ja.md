---
title: "`hyphens` プロパティの接頭辞が外れました"
date: "2015-09-15T09:19:00-04:00"
categories: ["css"]
tags: []
releases: ["43", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=953408"
      title: "Bug 953408 - Unprefix -moz-hyphens"
supported_tools:
  firefox_extension: true
---
[`hyphens`](https://developer.mozilla.org/docs/Web/CSS/hyphens) CSS プロパティの仕様が安定したため、接頭辞が外されました。接頭辞付きの `-moz-hyphens` プロパティは今のところ `hyphens` のエイリアスとして残されていますが、近い将来削除されます。
