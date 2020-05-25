---
title: "非標準のシステム測定擬似クラスとメディア特性が廃止されました"
date: "2017-10-06T10:12:00-04:00"
categories: ["css"]
tags: []
releases: ["58", "60-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1396066"
      title: "Bug 1396066 - Avoid exposing :-moz-system-metric stuff in content pages."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035774"
      title: "Bug 1035774 - Implement Interaction Media Features including pointer:coarse that replaces non-standard -moz-touch-enabled"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1406631"
      title: "Bug 1406631 - Remove color-picker-available system metric."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408838"
      title: "Bug 1408838 - Remove physical-home-button media feature."
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1408839"
      title: "Bug 1408839 - Hide some moz-scrollbar media features in content docs."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RVttfrQkXLU/discussion"
      title: "Intent to unship: :-moz-system-metric pseudo-class and media queries in content pages."
supported_tools:
  firefox_extension: true
---
非標準の `moz` 接頭辞付きシステム測定擬似クラスとメディア特性がウェブコンテンツから使用できなくなりました。これらの CSS 拡張仕様はフィンガープリンティング目的で悪用される可能性があったためです。

[`:-moz-system-metric(mac-graphite-theme)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(mac-graphite-theme))、[`:-moz-system-metric(scrollbar-end-backward)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(scrollbar-end-backward))、[`:-moz-system-metric(touch-enabled)`](https://developer.mozilla.org/docs/Web/CSS/:-moz-system-metric(touch-enabled)) など、`:-moz-system-metric` で始まる擬似クラスは廃止されました。

以下のメディア特性も併せて廃止されました。

* `-moz-color-picker-available`
* `-moz-is-glyph`
* [`-moz-mac-graphite-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-mac-graphite-theme)
* `-moz-mac-yosemite-theme`
* [`-moz-os-version`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-os-version)
* `-moz-overlay-scrollbars`
* `-moz-physical-home-button`
* [`-moz-scrollbar-end-backward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-end-backward)
* [`-moz-scrollbar-end-forward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-end-forward)
* [`-moz-scrollbar-start-backward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-start-backward)
* [`-moz-scrollbar-start-forward`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-start-forward)
* [`-moz-scrollbar-thumb-proportional`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-scrollbar-thumb-proportional)
* `-moz-swipe-animation-enabled`
* [`-moz-windows-accent-color-in-titlebar`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-accent-color-in-titlebar)
* [`-moz-windows-classic`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-classic)
* [`-moz-windows-compositor`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-compositor)
* [`-moz-windows-default-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-default-theme)
* [`-moz-windows-glass`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-glass)
* [`-moz-windows-theme`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-windows-theme)

唯一の例外は [`-moz-touch-enabled`](https://developer.mozilla.org/docs/Web/CSS/@media/-moz-touch-enabled) メディア特性で、これは標準の代替仕様となる [Interaction Media Features](https://drafts.csswg.org/mediaqueries-4/#mf-interaction) が Firefox に実装されるまで残されます。

**更新**: `-moz-touch-enabled` は [Firefox 71](https://www.fxsitecompat.dev/ja/docs/2019/moz-touch-enabled-media-feature-has-been-deprecated/) 以降廃止予定となっています。

**更新 2**: `-moz-touch-enabled` は [Firefox 73](https://www.fxsitecompat.dev/ja/docs/2019/moz-touch-enabled-media-feature-has-been-removed/) で廃止されました。
