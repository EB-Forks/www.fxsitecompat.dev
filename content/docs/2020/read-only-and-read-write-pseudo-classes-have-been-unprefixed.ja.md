---
title: "`:read-only` と `:read-write` 擬似クラスの接頭辞が外れました"
date: "2020-05-15T21:23:00-04:00"
categories: ["css"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=312971"
      title: "Bug 312971 - Support :read-only and :read-write pseudoclasses (unprefix)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=888884"
      title: "Bug 888884 - :-moz-read-write pseudo-class shouldn't be applied on <input type=text disabled> and <textarea disabled>"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/3CguC7Mp3yQ/discussion"
      title: "Intent to ship: :read-only / :read-write pseudo-classes"
supported_tools:
  firefox_extension: true
---
[`:read-only`](https://developer.mozilla.org/docs/Web/CSS/:read-only)、[`:read-write`](https://developer.mozilla.org/docs/Web/CSS/:read-write) CSS 擬似クラスが Firefox 78 以降で使用可能となりました。接頭辞付きの `:-moz-read-only`、`:-moz-read-write` 擬似クラスはエイリアスとして残されますが、将来的に対応は廃止されます。

Firefox 78 では `:read-write` の標準準拠問題も修正され、[HTML 仕様](https://html.spec.whatwg.org/#selector-read-write) に従い、無効化された `<input>` や `<textarea>` 要素には適用されなくなりました。
