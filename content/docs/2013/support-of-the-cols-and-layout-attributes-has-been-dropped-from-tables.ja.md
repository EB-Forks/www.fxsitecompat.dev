---
title: "`<table>` から `cols`、`layout` 両属性の実装が削除されました"
date: "2013-02-06T08:44:10-05:00"
categories: ["html"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=835169"
      title: "Bug 835169 – Do we need support for the table[cols] attribute?"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=835439"
      title: "Bug 835439 – Remove support for the table[layout] attribute"
aliases:
    - "/ja/docs/2013/support-of-the-cols-and-layout-properties-has-been-dropped-from-tables/"
---
Firefox は [`<table>`](https://developer.mozilla.org/docs/Web/HTML/Element/table) 要素上で `cols`、`layout` 属性を受け入れなくなりました。他のどのブラウザーもこれらの無名属性に対応していません。
