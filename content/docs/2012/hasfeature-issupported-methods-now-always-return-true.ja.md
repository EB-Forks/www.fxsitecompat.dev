---
title: "`hasFeature()`/`isSupported()` メソッドが常に `true` を返すようになりました"
date: "2012-12-03T03:54:45-05:00"
categories: ["dom"]
tags: []
releases: ["19", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=801425"
      title: "Bug 801425 – Make hasFeature() and isSupported() always return true"
---
[`document.implementation`](https://developer.mozilla.org/docs/DOM/document.implementation).hasFeature と [`Element.isSupported`](https://developer.mozilla.org/docs/DOM/Element.isSupported) の両メソッドが常に `true` を返すようになりました。これらは役に立たない API とみなされ仕様が変更されました。ただし SVG 機能に関しては例外で、従来通り実際の対応状況が返ります。

**更新**: `isSupported` メソッドは [Firefox 22](https://www.fxsitecompat.dev/ja/docs/2013/node-issupported-has-been-removed/) で廃止されました。

**更新 2**: SVG の例外は [Firefox 51](https://www.fxsitecompat.dev/ja/docs/2016/hasfeature-will-always-return-true-even-for-svg/) で廃止されました。
