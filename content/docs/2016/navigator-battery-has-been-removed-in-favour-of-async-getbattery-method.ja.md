---
title: "`navigator.battery` が非同期 `getBattery` メソッドに置き換えられる形で削除されました"
date: "2016-06-07T10:08:00-04:00"
categories: ["dom"]
tags: []
releases: ["50", "52-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1259335"
      title: "Bug 1259335 - Remove deprecated navigator.battery API"
supported_tools:
  firefox_extension: true
---
[Firefox 43 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2015/navigator-battery-has-been-deprecated-in-favour-of-async-getbattery-method/) [`navigator.battery`](https://developer.mozilla.org/docs/Web/API/Navigator/battery) プロパティが Firefox 50 で削除されました。代わりに、[`BatteryManager`](https://developer.mozilla.org/docs/Web/API/BatteryManager) インスタンスを得られる `Promise` を返す、標準化された [`navigator.getBattery`](https://developer.mozilla.org/docs/Web/API/Navigator/getBattery) メソッドを使ってください。

**更新**: Battery Status API は [Firefox 52 で削除されました](https://www.fxsitecompat.dev/ja/docs/2016/battery-status-api-has-been-removed/)。
