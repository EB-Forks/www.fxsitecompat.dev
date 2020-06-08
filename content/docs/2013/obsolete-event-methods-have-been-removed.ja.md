---
title: "古いイベントメソッドが削除されました"
date: "2013-05-19T07:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["24", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=673919"
      title: "Bug 673919 – Remove routeEvent, enableExternalCapture and disableExternalCapture"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=874003"
      title: "Bug 874003 – Remove preventBubble and preventCapture"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=726933"
      title: "Bug 726933 – Warn about getPreventDefault being deprecated"
supported_tools:
  firefox_extension: true
---
[`window`](https://developer.mozilla.org/docs/Web/API/window) オブジェクト上の [`routeEvent`](https://developer.mozilla.org/docs/Web/API/window.routeEvent)、`enableExternalCapture`、`disableExternalCapture` メソッドが削除されました。これらは Firefox 3 以降廃止予定となっていた非標準の Netscape 由来 API で、既に no-op (何も行わない) 実装となっていました。一方、[`captureEvents`](https://developer.mozilla.org/docs/Web/API/window.captureEvents) と [`releaseEvents`](https://developer.mozilla.org/docs/Web/API/window.releaseEvents) は後方互換性のために残されています。Google による調査で、多くのサイトが機能判別のためこれらのメソッドに依存していることが明らかになったためです。

初期の W3C 仕様案に含まれていた `preventBubble` と `preventCapture` メソッドも削除されました。[`stopPropagation`](https://developer.mozilla.org/docs/Web/API/event.stopPropagation) メソッドで代用可能です。

また、Firefox 16 以降廃止予定となっている非標準の `getPreventDefault` メソッドは、[`defaultPrevented`](https://developer.mozilla.org/docs/Web/API/event.defaultPrevented) プロパティに置き換えられたため、まもなく削除されます。`getPreventDefault` がウェブページ内で使用されていると、廃止予定についての警告が [ウェブコンソール](https://developer.mozilla.org/docs/Tools/Web_Console) 内に表示されます。
