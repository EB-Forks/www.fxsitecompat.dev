---
title: "`:is()` 擬似クラスの接頭辞が外れました"
date: "2020-05-24T16:50:00-04:00"
categories: ["css"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1509418"
      title: "Bug 1509418 - Implement `:is()` and `:where()` selectors"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632646"
      title: "Bug 1632646 - Enable :is() / :where() on all release channels."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/_f8gYPevIQw/discussion"
      title: "Intent to prototype and ship: CSS :is() and :where() pseudo-classes."
supported_tools:
  firefox_extension: true
---
[Selectors Level 4 仕様](https://drafts.csswg.org/selectors/) に含まれる [`:is()`](https://developer.mozilla.org/docs/Web/CSS/:is) と [`:where()`](https://developer.mozilla.org/docs/Web/CSS/:where) CSS 擬似クラスが Firefox 78 で有効化されました。Firefox では、`:is()` は長いこと `:-moz-any()` として実装されていました。接頭辞付き擬似クラスはまだ使用可能ですが、将来的に削除される可能性もあります。あなたのウェブサイトを時代遅れにしないよう、標準版と非標準版の両方を使うようにしましょう。
