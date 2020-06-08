---
title: "`File.mozFullPath` が削除されました"
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
非標準の [`File.mozFullPath`](https://developer.mozilla.org/docs/Web/API/File.mozFullPath) プロパティがウェブコンテンツから使用できなくなりました。
