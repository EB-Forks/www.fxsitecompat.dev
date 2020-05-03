---
title: "`<pre>` から古い機能が削除されました"
date: "2014-02-07T11:57:09-05:00"
categories: ["html"]
tags: []
releases: ["29", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949879"
      title: "Bug 949879 – Drop support for <pre cols>"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=950737"
      title: "Bug 950737 – Remove layout effect from <pre width>"
supported_tools:
  firefox_extension: true
---
Firefox は [`<pre>`](https://developer.mozilla.org/docs/Web/HTML/Element/pre) 要素の `cols`、`width` 両属性に対応しなくなりました。前者は Netscape Navigator 由来の非標準の拡張仕様でした。後者は HTML4 の仕様に含まれていましたが、[HTML5](https://developer.mozilla.org/docs/Web/Guide/HTML/HTML5) から削除されました。
