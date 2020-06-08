---
title: "`File.mozFullPath` has been removed"
date: "2014-10-17T22:50:44-04:00"
categories: ["dom"]
tags: []
releases: ["35", "38-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1048293"
      title: "Bug 1048293 – File::mozFullPath attribute should not be exposed to content."
supported_tools:
  firefox_extension: true
---
The non-standard [`File.mozFullPath`](https://developer.mozilla.org/docs/Web/API/File.mozFullPath) property is no longer available from Web content.
