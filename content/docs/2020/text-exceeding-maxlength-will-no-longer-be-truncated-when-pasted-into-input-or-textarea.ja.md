---
title: "`maxlength` を超えるテキストが `<input>` や `<textarea>` に貼り付けられた際に切り詰められなくなりました"
date: "2020-05-15T21:23:00-04:00"
categories: ["html"]
tags: []
releases: ["77"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1320229"
      title: "Bug 1320229 - Consider warning if a value pasted in a password field is truncated due to max length"
---
Firefox 77 以降、`<input>` や `<textarea>` HTML 要素は、貼り付けられたりドロップされたりしたユーザーテキストが [`maxlength`](https://developer.mozilla.org/docs/Web/HTML/Attributes/maxlength) で指定された文字数を超える場合であっても、それを自動的に切り詰めなくなります。この変更は主に、予期せず切り詰められたパスワードが保存されてしまうのを防ぐ目的で行われるものです。

テキストが `maxlength` より長かった場合、そのフォームコントロールは無効と判断されます。要素の [`validity`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/validity) DOM オブジェクトはそれを受けて更新され、`valid` プロパティは `false` に、`tooLong` プロパティは `true` に変わります。

ユーザーは通常、「テキストを 20 文字以下に短くしてください (現在 30 文字です)」といった検証メッセージととともに、テキスト入力欄の周りに赤い枠線を目にすることとなります。このメッセージの内容は、必要であれば [`setCustomValidity`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/setCustomValidity) メソッドを用いてカスタマイズできます。

ユーザーが問題を修正するまでフォームは送信できないため、サーバーが極端に長いテキストやパスワードを受け取ることはないはずです (サーバーサイドの検証はいずれにしても実装すべきです)。しかしこれは、入力されたテキストが決して `maxlength` を超えないことを想定したフロントエンド実装があった場合に潜在的な影響を与える可能性があります。
