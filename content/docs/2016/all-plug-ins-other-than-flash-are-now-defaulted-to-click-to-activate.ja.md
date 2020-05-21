---
title: "Flash 以外すべてのプラグインが初期設定で「クリックして有効化」になりました"
date: "2016-04-30T07:25:00-04:00"
categories: ["plugins"]
tags: []
releases: ["47", "52-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1263630"
      title: "Bug 1263630 - Remove all plugins (except Flash) from the click-to-activate whitelist"
---
[Firefox における NPAPI プラグイン廃止](https://www.fxsitecompat.dev/ja/docs/2015/plug-in-support-will-be-dropped-by-the-end-of-2016-except-flash/) の一環として、Adobe Flash Player を除くすべてのプラグインが [2014 年初めに導入されたプラグインホワイトリスト](https://www.fxsitecompat.dev/ja/docs/2014/plugin-whitelist-has-been-implemented/) から削除されました。つまり、それらは Firefox 47 以降、初期設定の「クリックして有効化」の挙動に戻ることになります。Flash 以外の NPAPI 対応は Firefox 53 で削除される予定となっていますので、ウェブ開発者の皆さんにはモダンな標準技術を代わりに使うよう強く推奨します。
