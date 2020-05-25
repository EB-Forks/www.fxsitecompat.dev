---
title: "`-moz-text-decoration-*` プロパティが削除されました"
date: "2015-04-27T13:17:23-04:00"
categories: ["css"]
tags: []
releases: ["40", "45-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1097922"
      title: "Bug 1097922 - Remove temporary aliases for -moz-text-decoration-*."
supported_tools:
  firefox_extension: true
---
[Firefox 36 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2014/css3-text-decoration-properties-have-been-unprefixed-text-decoration-becomes-a-shorthand/)、[`text-decoration-color`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-color)、[`text-decoration-line`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-line)、[`text-decoration-style`](https://developer.mozilla.org/docs/Web/CSS/text-decoration-style) 各プロパティの `moz` 接頭辞付き対応が削除されました。今後は接頭辞なしプロパティを使用してください。
