---
title: "`touchenter`、`touchleave` イベントが廃止されました"
date: "2014-07-22T05:06:26-04:00"
categories: ["dom"]
tags: []
releases: ["33", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1036444"
      title: "Bug 1036444 – Remove the NS_TOUCH_ENTER and NS_TOUCH_LEAVE events"
supported_tools:
  firefox_extension: true
---
[`touchenter`](https://developer.mozilla.org/docs/Web/Reference/Events/touchenter)、[`touchleave`](https://developer.mozilla.org/docs/Web/Reference/Events/touchleave) 両イベントへの対応が廃止されました。これらが [`TouchEvent`](https://developer.mozilla.org/docs/Web/API/TouchEvent) 仕様から削除されたためです。
