---
title: "`MouseEvent.movementX`/`Y` の接頭辞が外れました"
date: "2015-06-13T15:20:46-04:00"
categories: ["dom"]
tags: []
releases: ["41", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1164981"
      title: "Bug 1164981 - Add MouseEvent.movementX/Y"
---
[`MouseEvent.movementX`](https://developer.mozilla.org/docs/Web/API/MouseEvent/movementX)、[`MouseEvent.movementY`](https://developer.mozilla.org/docs/Web/API/MouseEvent/movementY) 両プロパティの接頭辞が外れました。`moz` 接頭辞付きプロパティは将来的に削除されます。

**更新**: これらのプロパティは [Firefox 50](https://www.fxsitecompat.dev/ja/docs/2016/prefixed-pointer-lock-api-has-been-removed/) で廃止されました。
