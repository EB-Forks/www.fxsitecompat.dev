---
title: "`@-moz-document` 対応が空の `url-prefix()` を除いて打ち切られました"
date: "2018-03-18T16:09:00-04:00"
categories: ["css", "privacy-security"]
tags: []
releases: ["61", "68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1035091"
      title: "Bug 1035091 - limit @-moz-document to user and UA sheets (Makes it useless for exfiltration in CSS-injection attacks)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1422245"
      title: "Bug 1422245 - Toggle the pref to disable @-moz-document in content pages on release"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1446470"
      title: "Bug 1446470 - Parse @-moz-document url-prefix() on content."
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/RysotXvooV0/discussion"
      title: "Intent to unship: @-moz-document from content pages."
aliases:
    - "/ja/docs/2015/moz-document-support-has-been-dropped/"
    - "/ja/docs/2015/moz-document-support-will-be-dropped/"
    - "/ja/docs/2018/moz-document-has-been-dropped/"
supported_tools:
  firefox_extension: true
---
[`@-moz-document`](https://developer.mozilla.org/docs/Web/CSS/@document) ルールがウェブコンテンツから使用できなくなりました。これは、第三者サイトの URL に含まれる機密データを盗み出す目的で、攻撃者による CSS インジェクションに悪用される恐れがあったためです。Firefox ユーザーは引き続きユーザースタイルシート内でこのルールを使い、ブラウジング体験をパーソナライズすることが可能です。

この @ 規則対応は Firefox 59 の時点で既に Nightly と早期 Beta/DevEdition から削除されており、Firefox 61 ですべてのチャンネルから削除されました。

例外は、[Firefox を対象とした CSS ハック](https://css-tricks.com/snippets/css/css-hacks-targeting-firefox/) として使われてきた空の `url-prefix` 関数です。これは問題を避けるため Release チャンネルでは引き続きパースされますが、近い将来主な互換性問題が解決したら削除されます。
