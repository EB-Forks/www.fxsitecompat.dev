---
title: "`window.external.AddSearchProvider()` is now a dummy function"
date: "2020-05-23T18:35:00-04:00"
categories: ["dom"]
tags: []
releases: ["78"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1632447"
      title: "Bug 1632447 - Disable window.{external|sidebar}.AddSearchProvider by preference"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/vSV-gg5621k/discussion"
      title: "Intent to unship: window.external.AddSearchProvider"
---
Starting with Firefox 78, `window.external.AddSearchProvider` and the alias `window.sidebar.AddSearchProvider` will be dummy functions that do nothing, according to the [HTML spec](https://html.spec.whatwg.org/multipage/obsolete.html#external). The Internet Explorer-derived legacy method had been deprecated since [Firefox 65](https://www.fxsitecompat.dev/en-CA/docs/2018/window-sidebar-and-window-external-addsearchprovider-have-been-deprecated/). Google made it no-op with [Chrome 54](https://www.chromestatus.com/feature/5672001305837568) in October 2016, and no other modern browsers support it.

If your website would like to provide a custom search provider, there are still two ways to do so:

* Support [search provider auto-discovery](https://developer.mozilla.org/docs/Web/OpenSearch#Autodiscovery_of_search_plugins) on your site, using `<link rel="search">`
* Create a browser extension that adds a search provider, using the [`chrome_settings_overrides`](https://developer.mozilla.org/docs/Mozilla/Add-ons/WebExtensions/manifest.json/chrome_settings_overrides) manifest key

The Netscape-derived, non-standard `window.sidebar` object will be [removed in the near future](https://www.fxsitecompat.dev/en-CA/docs/2015/window-sidebar-will-be-removed/).
