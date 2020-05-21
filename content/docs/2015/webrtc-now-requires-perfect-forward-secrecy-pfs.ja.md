---
title: "WebRTC で Perfect Forward Secrecy (PFS) が必須となりました"
date: "2015-02-27T04:21:22-05:00"
categories: ["privacy-security"]
tags: []
releases: ["38", "38-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1052610"
      title: "Bug 1052610 – WebRTC: Allow more ciphers for DTLS 1.2 in Firefox Nightly 34.0a1 (cannot perform DTLS with OpenSSL)"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1134437"
      title: "Bug 1134437 – Delay move to PFS cipher suites"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1158343"
      title: "Bug 1158343 – Temporarily re-enable TLS_RSA_WITH_AES_128_CBC_SHA for WebRTC"
---
Firefox 38 以降、[WebRTC](https://developer.mozilla.org/docs/Web/Guide/API/WebRTC) で通信をより安全にするため Perfect Forward Secrecy (PFS) 暗号化スイートのいずれかが必須となりました。詳しくは [Mozilla Hacks ブログ](https://hacks.mozilla.org/2015/02/webrtc-requires-perfect-forward-secrecy-pfs-starting-in-firefox-38/) を参照してください。*Facebook メッセンジャー* との相互運用性問題から、`TLS_RSA_WITH_AES_128_CBC_SHA` スイートのみ再度一時的に有効化され、Firefox 39 で無効化されます。
