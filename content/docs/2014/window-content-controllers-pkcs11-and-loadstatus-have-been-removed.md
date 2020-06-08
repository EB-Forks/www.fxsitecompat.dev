---
title: "`window._content`, `controllers`, `pkcs11` and `LoadStatus` have been removed"
date: "2014-02-07T11:57:09-05:00"
categories: ["dom"]
tags: []
releases: ["29"]
statuses: "reverted"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=946564"
      title: "Bug 946564 – Make window._content chromeonly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=794943"
      title: "Bug 794943 – Remove nsISecurityCheckedComponent"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=964964"
      title: "Bug 964964 – Try to remove window.pkcs11"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=949292"
      title: "Bug 949292 – Stop exposing LoadStatus on the global object"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1010137"
      title: "Bug 1010137 – RAP application does not start in Firefox 29"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1010577"
      title: "Bug 1010577 – Add back window.controllers for site compatibility"
supported_tools:
  firefox_extension: true
---
As part of the ongoing effort to standardize global objects, some properties have been removed from [`window`](https://developer.mozilla.org/docs/Web/API/window). The `_content` property is no longer available from Web content in favour of [`window.content`](https://developer.mozilla.org/docs/Web/API/window.content). The [`window.pkcs11`](https://developer.mozilla.org/docs/Web/API/window.pkcs11) property has returned `null` since Firefox 3.0.14 for security reasons. The non-standard [`controllers`](https://developer.mozilla.org/docs/Web/API/window.controllers) property and `LoadStatus` interface are also no longer available on `window`.

**Update**: Apps using Eclipse Remote Application Platform (RAP) have to [update the code](https://wiki.eclipse.org/RAP/FAQ#Blank_page_or_client_crash_in_Firefox_29.2B) since the framework was using the removed `window.controllers` property to detect Firefox. Since `window.controllers` is still [widely used](https://github.com/search?q=%22window.controllers%22+Gecko&type=Code) for the same user agent detection purpose, the property has been added back to Firefox 30.
