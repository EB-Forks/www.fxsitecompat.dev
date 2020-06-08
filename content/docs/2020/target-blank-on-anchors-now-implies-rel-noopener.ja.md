---
title: "アンカー上の `target=_blank` が `rel=noopener` を暗示するようになりました"
date: "2020-06-07T22:43:00-04:00"
categories: ["dom", "html", "privacy-security"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1503681"
      title: "Bug 1503681 - Make target=_blank on anchors imply rel=noopener"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1522083"
      title: "Bug 1522083 - Make target=_blank on a/area elements imply rel=noopener by default"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/DDQP5xIKYiY/discussion"
      title: "Intent to ship: implicit ref=noopener for target=_blank on anchor and area elements"
---
Firefox 79 以降、`target="_blank"` を伴った `<a>` や `<area>` 要素は、[現行の HTML 仕様](https://github.com/whatwg/html/issues/4078) に従い、`rel` 属性が設定されていない限り暗黙的に `rel="noopener"` を適用します。[`noopener`](https://developer.mozilla.org/docs/Web/HTML/Link_types/noopener) リンクタイプは新たに開かれたウィンドウ内の [`window.opener`](https://developer.mozilla.org/docs/Web/API/Window/opener) を `null` とすることで、この DOM プロパティが信頼できない第三者のサイトによって悪用されるのを防ぎます。必要な場合は、`rel="opener"` を明示的に設定することで挙動を反転させられます。

Apple は 2019 年 3 月公開の [Safari 12.1](https://developer.apple.com/documentation/safari_release_notes/safari_12_1_release_notes) で最初にこの変更を行いました。Firefox では、Firefox 65 以降の Nightly と早期 Beta チャンネルにおいてこの新しい挙動が初期設定で有効となっています。[Google Chrome](https://bugs.chromium.org/p/chromium/issues/detail?id=898942) も後に続く見込みです。
