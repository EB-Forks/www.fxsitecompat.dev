---
title: "`window.content` が削除されます"
date: "2017-09-13T07:19:00-04:00"
categories: ["dom"]
tags: []
releases: ["future"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=864845"
      title: "Bug 864845 - Make window.content chrome-only in nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1400140"
      title: "Bug 1400140 - Make window.content chrome-only"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632143"
      title: "Bug 1632143 - Make window.content chrome-only in early betas"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/Tmbs-wFwHzo/discussion"
      title: "Intent to unship: Visibility of window.content to untrusted code"
aliases:
    - "/ja/docs/2017/window-content-has-been-removed/"
supported_tools:
  firefox_extension: true
---
非標準の [`window.content`](https://developer.mozilla.org/docs/Web/API/Window/content) オブジェクトは Firefox Nightly 57 以降ウェブコンテンツから使用できなくなりました。[Telemetry](https://telemetry.mozilla.org/) で使用頻度が低いことが確認され次第、他のチャンネルからも削除されます。

このオブジェクトは [`window.top`](https://developer.mozilla.org/docs/Web/API/Window/top) あるいは多くの場合単純に [`window`](https://developer.mozilla.org/docs/Web/API/Window) のエイリアスに過ぎないため有用ではありませんが、[Firefox 29](https://www.fxsitecompat.dev/ja/docs/2014/window-content-controllers-pkcs11-and-loadstatus-have-been-removed/) で一度削除されたものの後方互換性を保つため再度追加された [`window.controllers`](https://developer.mozilla.org/docs/Web/API/Window/controllers) のように、ウェブ上ではブラウザー判別目的で誤用されている可能性があります。ウェブ開発者は常にこうした非標準機能の使用を避けるべきです。

**更新**: Firefox 77 以降、`window.content` は早期ベータ版でも無効化されています。
