---
title: "`<keygen>` 対応が廃止されました"
date: "2019-06-13T20:06:00-04:00"
categories: ["dom", "html", "privacy-security"]
tags: []
releases: ["69"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1315460"
      title: "Bug 1315460 - Remove support for HTML Keygen"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/SAh1b1R5lrY/discussion"
      title: "Intent to unship: <keygen>"
aliases:
    - "/ja/docs/2017/keygen-support-has-been-dropped/"
    - "/ja/docs/2018/keygen-support-will-be-dropped/"
supported_tools:
  firefox_extension: true
---
非標準の [`<keygen>`](https://developer.mozilla.org/docs/Web/HTML/Element/keygen) HTML 要素と [`HTMLKeygenElement`](https://developer.mozilla.org/docs/Web/API/HTMLKeygenElement) DOM インターフェイスへの対応は Firefox 69 で削除されました。この公開鍵生成機能は Internet Explorer では一度も実装されたことがなく、Google Chrome は 2017 年 3 月公開の [バージョン 57](https://www.chromestatus.com/feature/5716060992962560) で既に対応を廃止しています。代わりに標準の [Web Crypto API](https://developer.mozilla.org/docs/Web/API/Web_Crypto_API) と [Web Authentication API](https://developer.mozilla.org/docs/Web/API/Web_Authentication_API) を使用してください。
