---
title: "Firefox 78 Beta と Developer Edition が公開、次期 ESR のベースに"
date: "2020-06-02T22:30:00-04:00"
---
Mozilla は今日 [Firefox 78 Beta と Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) を公開しました。私たちはこの次回リリースに向けて [3 件の互換性記事](https://www.fxsitecompat.dev/ja/releases/78/) を投稿していますが、うち 2 つは接頭辞の解除、残る 1 つはめったに使われないメソッドであるため、あなたのサイトに影響を与えるものは何もないはずです。

Firefox 78 は次期 [延長サポート版](https://support.mozilla.org/kb/choosing-firefox-update-channel) (ESR) となり、法人向けに 1 年間維持されます。通常の高速リリースと同じ 7 月 28 日に公開され次第、私たちは Firefox 78 ESR サイト互換性情報のページを用意します。良い知らせとしては、Firefox エンジニアが [従来 ESR では無効化されていた](https://www.fxsitecompat.dev/ja/docs/2019/service-workers-and-push-notifications-are-disabled-on-firefox-68-esr/) Service Worker API やプッシュ通知を有効化を検討中です。この決定はまもなく確認されます。

社会が少しずつ再開しつつあることから、互換性を破るような一部の変更はおそらく Firefox 79 で戻ってくるでしょう。目下 COVID-19 の世界的流行により、以下の重要な変更が延期されています。

* [TLS 1.0/1.1 対応の廃止](https://www.fxsitecompat.dev/ja/docs/2020/tls-1-0-1-1-support-has-been-removed/)
* [WebRTC の DTLS 1.0 対応の廃止](https://www.fxsitecompat.dev/ja/docs/2020/dtls-1-0-support-in-webrtc-has-been-removed/)
* [FTP 対応の廃止](https://www.fxsitecompat.dev/ja/docs/2020/ftp-support-will-be-removed/)
* [Application Cache ストレージの廃止](https://www.fxsitecompat.dev/ja/docs/2020/application-cache-storage-has-been-removed/)
* [ワーカースクリプトの MIME 判別強制](https://www.fxsitecompat.dev/ja/docs/2020/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/)
* Cookie の `SameSite=Lax` デフォルト採用

また、年末までに [Flash 対応が廃止される](https://www.fxsitecompat.dev/ja/docs/2018/flash-plug-in-support-will-be-removed-in-2020/) ことも忘れないでください。必ず前もって計画を立てるようにしましょう。

**更新**: Mozilla は Firefox 78 で TLS 1.0/1.1 を無効化する予定です。
