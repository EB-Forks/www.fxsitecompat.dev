---
title: "いくつかの API から接頭辞が外れました"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=726378"
      title: "Bug 726378 – Unprefix IndexedDB"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=769571"
      title: "Bug 769571 – Unprefix battery and vibrator APIs"
supported_tools:
  firefox_extension: true
---
[IndexedDB](https://developer.mozilla.org/docs/Web/API/IndexedDB_API) API から接頭辞が外れました。今後は `mozIndexedDB` ではなく標準の [`indexedDB`](https://developer.mozilla.org/docs/Web/API/IDBEnvironment/indexedDB) オブジェクトを使用できます。

[バッテリーステータス](https://developer.mozilla.org/docs/Web/API/Battery_Status_API)、[バイブレーション](https://developer.mozilla.org/docs/Web/API/Vibration_API) の各 API についても接頭辞が外れています。接頭辞付きの `navigator.mozBattery`、`navigator.mozVibrate` 両メソッドは今後使用できません。

**更新**: `mozIndexedDB` オブジェクトは [Firefox 38](https://www.fxsitecompat.dev/ja/docs/2015/mozindexeddb-has-been-removed/) で削除されました。

**更新 2**: Battery Status API は [Firefox 52](https://www.fxsitecompat.dev/ja/docs/2016/battery-status-api-has-been-removed/) で削除されました。
