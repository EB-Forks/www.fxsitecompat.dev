---
title: "サイドバーパネル追加機能が削除されました"
date: "2013-04-06T04:52:59-04:00"
categories: ["dom"]
tags: []
releases: ["23", "24-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=691647"
      title: "Bug 691647 – clean up nsISidebar (remove window.sidebar.addPanel/addPersistentPanel)"
supported_tools:
  firefox_extension: true
---
`window.sidebar.addPanel` と `window.sidebar.addPersistentPanel` の対応が削除されました。これらのメソッドは、ウェブパブリッシャーが自社コンテンツをブラウザーのサイドバーパネルとして統合できるようにしていた Netscape 由来 API の一部でした。これらは標準化されず、めったに使用されず、ブラウザー側の対応も不十分なままでした。他のどのブラウザーもこれらのメソッドを実装していません。

今後 [`window.sidebar`](https://developer.mozilla.org/docs/Web/API/window.sidebar) 自体を削除する [計画](https://www.fxsitecompat.dev/ja/docs/2015/window-sidebar-will-be-removed/) もあります。

これらの API の代わりとして、[eBay Sidebar](https://addons.mozilla.org/firefox/addon/ebay-sidebar/) のように [サイドバー拡張機能を作成する](https://developer.mozilla.org/docs/Creating_a_Firefox_sidebar)、あるいは [Facebook Messenger](https://www.facebook.com/about/messenger-for-firefox) のように [Social API を活用する](https://developer.mozilla.org/docs/Social_API) ことができます。
