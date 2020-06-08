---
title: "`Element.matches()` の接頭辞が外れました"
date: "2014-09-01T22:12:15-04:00"
categories: ["dom"]
tags: []
releases: ["34", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=886308"
      title: "Bug 886308 – Implement Element.matches()"
---
[`Element.matches`](https://developer.mozilla.org/docs/Web/API/Element.matches) メソッドの仕様が安定したと見なされることから、ようやく接頭辞が外れました。接頭辞付きの `mozMatchesSelector` メソッドは [将来的に削除されます](https://www.fxsitecompat.dev/ja/docs/2015/element-mozmatchesselector-will-be-removed/)。
