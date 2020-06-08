---
title: "Page Visibility API の接頭辞が外れました"
date: "2012-12-03T03:53:26-05:00"
categories: ["dom"]
tags: []
releases: ["18", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=812086"
      title: "Bug 812086 – Unprefix Page Visibility API"
---
接頭辞付きの `mozvisibilitychange` イベントと、[Page Visibility API](https://developer.mozilla.org/docs/DOM/Using_the_Page_Visibility_API) の `mozHidden`、`mozVisibilityState` プロパティが廃止予定となりました。今後は接頭辞なしの [`visibilitychange`](https://developer.mozilla.org/docs/Mozilla_Event_Reference/visibilitychange) イベントと、[`hidden`](https://developer.mozilla.org/docs/DOM/Using_the_Page_Visibility_API#document.hidden)、[`visibilityState`](https://developer.mozilla.org/docs/DOM/Using_the_Page_Visibility_API#document.visibilityState) プロパティを使用してください。

**更新**: 接頭辞付き API は [Firefox 51](https://www.fxsitecompat.dev/ja/docs/2016/prefixed-page-visibility-api-has-been-removed/) で削除されました。
