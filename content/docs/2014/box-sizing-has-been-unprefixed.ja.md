---
title: "`box-sizing` の接頭辞が外れました"
date: "2014-02-07T11:57:09-05:00"
categories: ["css"]
tags: []
releases: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=243412"
      title: "Bug 243412 – Implement \'box-sizing\' (dropping the -moz- prefix)"
supported_tools:
  firefox_extension: true
---
[`box-sizing`](https://developer.mozilla.org/docs/Web/CSS/box-sizing) プロパティの接頭辞が外れました。`-moz-box-sizing` は一定期間残されますが、開発者は接頭辞なしのプロパティを代わりに使うことが推奨されます。
