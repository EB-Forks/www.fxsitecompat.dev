---
title: "`java` オブジェクトが削除されました"
date: "2012-10-09T06:00:00-04:00"
categories: ["dom"]
tags: []
releases: ["16"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=748343"
      title: "Bug 748343 – remove support for “java” DOM object"
supported_tools:
  firefox_extension: true
---
`window.java` と `window.packages` の各グローバル DOM オブジェクトが廃止されました。これらのオブジェクトはほとんど文書化されておらず、実際に使われることはまれかと思います。この変更は Firefox 15 で行われる予定でしたが、既存の Firefox 拡張機能との互換性を保つため [延期](https://bugzilla.mozilla.org/show_bug.cgi?id=778073) されていました。
