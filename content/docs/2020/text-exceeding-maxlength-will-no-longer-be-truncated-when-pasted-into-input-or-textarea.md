---
title: "Text exceeding `maxlength` will no longer be truncated when pasted into `<input>` or `<textarea>`"
date: "2020-05-15T21:23:00-04:00"
categories: ["html"]
tags: []
releases: ["77"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1320229"
      title: "Bug 1320229 - Consider warning if a value pasted in a password field is truncated due to max length"
---
Starting with Firefox 77, `<input>` and `<textarea>` HTML elements will no longer automatically truncate pasted or dropped user text, even if the content is longer than the number of characters specified with the [`maxlength`](https://developer.mozilla.org/docs/Web/HTML/Attributes/maxlength) attribute. This change mainly aims at preventing an unexpectedly truncated password from being saved.

The form control will be marked as invalid if the text is longer than `maxlength`. The element’s [`validity`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/validity) DOM object will be updated accordingly, where the `valid` property will be `false`, and the `tooLong` property will be `true`.

The user will typically see a red border around the text field along with a validation message like “Please shorten this text to 20 characters or less (you are currently using 30 characters),” that can be customized with the [`setCustomValidity`](https://developer.mozilla.org/docs/Web/API/HTMLObjectElement/setCustomValidity) method if needed.

The form cannot be submitted until the user fixes the error, so the server shouldn’t receive an excessively long text or password (a server-side validation has to be put in place anyway.) However, this could potentially affect a front-end implementation if it expects the entered text never to exceed `maxlength`.
