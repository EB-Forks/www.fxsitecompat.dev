---
title: "`scrollWidth` と `scrollHeight` が `overflow:visible` の影響を受けなくなりました"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=833542"
      title: "Bug 833542 – scrollWidth, scrollHeight different when overflow is hidden versus visible"
---
従来、要素に CSS `overflow:visible` が指定されていた場合、[`scrollWidth`](https://developer.mozilla.org/docs/Web/API/element.scrollWidth)、[`scrollHeight`](https://developer.mozilla.org/docs/Web/API/element.scrollHeight) 両プロパティに誤った値が設定される場合がありました。`overflow:hidden` が指定されていた場合との値と一致するよう、この挙動が修正されました。
