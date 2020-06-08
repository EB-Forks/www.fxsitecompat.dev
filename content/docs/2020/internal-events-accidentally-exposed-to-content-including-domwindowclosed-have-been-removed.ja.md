---
title: "誤ってコンテンツに露呈されていた `DOMWindowClosed` などの内部イベントが削除されました"
date: "2020-06-03T00:47:00-04:00"
categories: ["dom"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557407"
      title: "Bug 1557407 - Don't expose the `DOMWindowClosed` event to content"
supported_tools:
  firefox_extension: true
---
12 を超える非標準の内部イベントがウェブに露呈されていたことに Firefox 開発者が気が付きました。概して意図しないものでしたが、一部はテスト目的で実装されたものでした。Firefox 79 以降、これらのイベントはウェブコンテンツから使用できなくなります。

* `DOMWindowClose`: 新しいタブやポップアップイベントが `window.close()` で閉じられようとした際に発生していました
* `fullscreen`: [`fullscreenchange`](https://developer.mozilla.org/docs/Web/API/Element/fullscreenchange_event) とは別物です
* `MozBeforeInitialXULLayout`
* `MozMouseScrollFailed`
* `MozMouseScrollTransactionTimeout`
* `MozPaintWait`
* `MozPaintWaitFinished`
* `MozPerformDelayedBlur`
* `occlusionstatechange`
* `resolutionchange`
* `willenterfullscreen`
* `willexitfullscreen`
* `XULAlertClose`
