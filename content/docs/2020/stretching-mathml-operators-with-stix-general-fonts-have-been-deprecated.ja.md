---
title: "STIX General フォントによる伸縮 MathML 演算子が廃止予定となりました"
date: "2020-06-04T22:11:00-04:00"
categories: ["misc"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1630935"
      title: "Bug 1630935 - Add use counter and deprecation warning for STIXGeneral fonts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ufT7Oc42MEc/discussion"
      title: "Intent to deprecate: stretching MathML operators with STIXGeneral fonts"
---
Firefox 79 以降、STIX General フォントを用いた伸縮 MathML 演算子への対応が廃止予定となり、Nightly チャンネルでは初期設定で無効化されます。ニュースグループへの投稿によれば、それらのフォントは後に OpenType MATH フォントで解決された問題に対する「一時しのぎの解決策」でした。

STIX General フォントへの対応は [Firefox 41](https://www.fxsitecompat.dev/ja/docs/2015/mathml-default-font-has-been-changed/) 以降廃止予定となっており、将来的に削除されます。
