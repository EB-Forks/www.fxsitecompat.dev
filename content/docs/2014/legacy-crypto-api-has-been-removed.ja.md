---
title: "旧式 Crypto API が削除されました"
date: "2014-10-17T22:50:44-04:00"
categories: ["privacy-security"]
tags: []
releases: ["35", "38-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1030963"
      title: "Bug 1030963 – remove proprietary window.crypto functions/properties"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1083118"
      title: "Bug 1083118 – window.crypto.signText replacement"
---
[`window.crypto`](https://developer.mozilla.org/docs/Web/API/window.crypto) 上に実装されていた Netscape 由来の [旧式 Crypto API](https://developer.mozilla.org/docs/JavaScript_crypto) が、標準 [Web Crypto API](https://developer.mozilla.org/docs/Web/API/SubtleCrypto) の実装に伴って削除されました。これには、`enableSmartCardEvents`、`version` プロパティ、`generateCRMFRequest`、`importUserCertificates`、`logout`、`signText` メソッドが含まれます。詳細は [MozillaWiki の記事](https://wiki.mozilla.org/SecurityEngineering/Removing_Proprietary_window.crypto_Functions) を参照してください。

この旧式 API は [Firefox 33 で無効化](https://www.fxsitecompat.dev/ja/docs/2014/legacy-crypto-api-has-been-disabled/) されましたが、未だに様々な銀行や行政機関で使われていることから Firefox 34 で再び有効化されました。今回のバージョンで API は完全に削除されましたが、まだそうしたサイトを使う必要のあるユーザーは [signTextJS 拡張機能](https://addons.mozilla.org/firefox/addon/signtextjs/) で代用可能です。
