---
title: "Sherlock 検索プラグイン対応が打ち切られました"
date: "2015-09-23T16:29:00-04:00"
categories: ["misc"]
tags: []
releases: ["44", "45-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862137"
      title: "Bug 862137 - stop supporting Sherlock search engines"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=862148"
      title: "Bug 862148 - stop supporting installation of Sherlock plugins from the web"
aliases:
    - "/ja/docs/2015/sherlock-search-plugin-is-no-longer-supported/"
---
[Firefox 24 以降廃止予定となっていた](https://www.fxsitecompat.dev/ja/docs/2013/support-for-sherlock-search-plug-ins-has-been-deprecated/) 旧式 Sherlock 検索プラグイン形式への対応が Firefox 44 で廃止されました。[`window.sidebar.addSearchEngine`](https://developer.mozilla.org/docs/Web/API/Window/sidebar/Adding_search_engines_from_Web_pages#Installing_Sherlock_plugins) メソッドは、ウェブコンテンツから Sherlock のインストールが要求された場合、ウェブコンソールに警告を残すのみとなりました。

`addSearchEngine` メソッドはまだ [OpenSearch プラグイン](https://developer.mozilla.org/docs/Web/OpenSearch) に対応していますが、[`window.sidebar`](https://developer.mozilla.org/docs/Web/API/Window/sidebar) オブジェクトは [将来的に完全に削除されます](https://www.fxsitecompat.dev/ja/docs/2015/window-sidebar-will-be-removed/) ので、代わりに [`window.external.AddSearchProvider`](https://developer.mozilla.org/docs/Web/API/Window/sidebar/Adding_search_engines_from_Web_pages#Installing_OpenSearch_plugins) メソッドを使ってください。

**更新**: `addSearchEngine` メソッドは [Firefox 59 で削除されました](https://www.fxsitecompat.dev/ja/docs/2018/window-sidebar-addsearchengine-has-been-removed/)。
