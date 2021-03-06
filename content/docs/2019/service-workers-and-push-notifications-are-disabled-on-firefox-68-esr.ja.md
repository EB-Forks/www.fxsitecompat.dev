---
title: "Firefox 68 ESR では Service Worker とプッシュ通知が無効化されます"
date: "2019-06-06T23:19:00-04:00"
categories: ["dom"]
tags: []
releases: ["68-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1557565"
      title: "Bug 1557565 - Disable Service Workers and push under ESR68 but not under Fennec"
---
[Service Worker API](https://developer.mozilla.org/docs/Web/API/Service_Worker_API) と [Push API](https://developer.mozilla.org/docs/Web/API/Push_API) は、ブラウザー内での複数コンテンツプロセスへ適切に対応するための設計変更が続いていることから、[Firefox 45](https://www.fxsitecompat.dev/ja/docs/2016/service-workers-have-been-disabled-in-firefox-45-esr/)、[Firefox 52](https://www.fxsitecompat.dev/ja/docs/2017/service-workers-and-push-notifications-are-disabled-on-firefox-52-esr/)、[Firefox 60](https://www.fxsitecompat.dev/ja/docs/2018/service-workers-and-push-notifications-are-disabled-on-firefox-60-esr/) ESR と同様に Firefox 68 [延長サポート版](https://www.mozilla.org/firefox/organizations/) (ESR) 上でも引き続き無効化されることとなりました。Firefox ESR は主に大企業や大学内での一括導入向けです。これらの API は通常の Release チャンネルおよび Android 版では使用可能です。
