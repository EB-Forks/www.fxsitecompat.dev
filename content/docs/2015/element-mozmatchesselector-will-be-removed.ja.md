---
title: "`Element.mozMatchesSelector()` が削除されます"
date: "2015-10-26T20:21:00-07:00"
categories: ["dom"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1119718"
      title: "Bug 1119718 - Remove mozMatchesSelector"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1216193"
      title: "Bug 1216193 - Implement webkitMatchesSelector"
---
`Element.mozMatchesSelector` メソッドが、[Firefox 34](https://www.fxsitecompat.dev/ja/docs/2014/element-matches-has-been-unprefixed/) 以降使用可能な標準の [`Element.matches`](https://developer.mozilla.org/docs/Web/API/Element/matches) メソッドに置き換えられる形で将来的に削除されます。ウェブ相互運用性のため標準化された `webkitMatchesSelector` も Firefox 44 で実装されていますが、接頭辞なしのメソッドが常に推奨されます。
