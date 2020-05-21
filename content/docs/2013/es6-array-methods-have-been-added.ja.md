---
title: "ES6 の配列メソッドが追加されました"
date: "2013-07-14T19:12:37-04:00"
categories: ["javascript"]
tags: []
releases: ["25", "31-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=885553"
      title: "Bug 885553 – Implement ES6 Array.prototype.find and Array.prototype.findIndex"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=866849"
      title: "Bug 866849 – Implement ES6 Array.from and Array.of"
---
[ECMAScript 6 対応](https://developer.mozilla.org/docs/Web/JavaScript/ECMAScript_6_support_in_Mozilla) の一環として、[`Array.find`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/find)、[`Array.findIndex`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/findIndex)、[`Array.of`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/of) メソッドが追加されました。[`Array.from`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/from) もまもなく追加されます。これにより、[`Array.prototype`](https://developer.mozilla.org/docs/Web/JavaScript/Reference/Global_Objects/Array/prototype) を独自メソッドで拡張している一部 JavaScript ライブラリが動作しなくなる可能性があります。今のところ、少なくともひとつのライブラリ ([*Sugar*](https://bugzilla.mozilla.org/show_bug.cgi?id=903755)) が影響を受けることが分かっています。*Sugar* ユーザーは、この不一致を避けるため、最新版へ更新してください。
