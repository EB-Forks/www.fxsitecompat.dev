---
title: "`RegExp` の `global`、`ignoreCase`、`multiline`、`sticky` プロパティがプロトタイプアクセサプロパティになりました"
date: "2015-02-27T04:21:22-05:00"
categories: ["javascript"]
tags: []
releases: ["38", "38-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1120169"
      title: "Bug 1120169 - Implement RegExp.prototype.{global, ignoreCase, multiline, source, sticky, unicode}"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1138325"
      title: "Bug 1138325 - Turning RegExp#source from an instance property into an accessor breaks ClojureScript apps"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1150297"
      title: "Bug 1150297 - Move source property to RegExp instance again."
---
[`RegExp`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/RegExp) インスタンスプロパティの [`global`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global)、[`ignoreCase`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase)、[`multiline`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline)、[`sticky`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky) がプロトタイプアクセサへ移され、[`RegExp.prototype.global`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/global)、[`RegExp.prototype.ignoreCase`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/ignoreCase)、[`RegExp.prototype.multiline`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/multiline)、[`RegExp.prototype.sticky`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/sticky) となりました。[`source`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Regexp/source) プロパティへの変更はウェブ互換性の問題により [Firefox 41 へ延期されました](https://www.fxsitecompat.dev/ja/docs/2015/regexp-source-has-become-prototype-accessor-property/)。
