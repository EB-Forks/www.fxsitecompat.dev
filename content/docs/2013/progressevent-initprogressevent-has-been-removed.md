---
title: "`ProgressEvent.initProgressEvent()` has been removed"
date: "2013-02-24T03:44:31-05:00"
categories: ["dom"]
tags: []
releases: ["22", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=843489"
      title: "Bug 843489 – [Progress Events] Remove support for ProgressEvent.initProgressEvent() and Document.createEvent(\"ProgressEvent\")"
supported_tools:
  firefox_extension: true
---
The [`ProgressEvent.initProgressEvent`](https://developer.mozilla.org/docs/Web/API/ProgressEvent.initProgressEvent) method is no longer available, due to the removal from the spec. The support for `document.createEvent("ProgressEvent")` has also been dropped.
