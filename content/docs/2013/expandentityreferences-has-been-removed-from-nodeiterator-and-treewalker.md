---
title: "`expandEntityReferences` has been removed from `NodeIterator` and `TreeWalker`"
date: "2013-02-06T08:44:10-05:00"
categories: ["dom"]
tags: []
releases: ["21", "24-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=672190"
      title: "Bug 672190 – consider removing expandEntityReferences from NodeIterator and TreeWalker"
supported_tools:
  firefox_extension: true
---
The [`expandEntityReferences`](https://developer.mozilla.org/docs/Web/API/NodeIterator.expandEntityReferences) property, which returned a flag indicating whether or not the children of entity reference nodes were visible to the object, has been removed from the [`NodeIterator`](https://developer.mozilla.org/docs/Web/API/NodeIterator) and [`TreeWalker`](https://developer.mozilla.org/docs/Web/API/TreeWalker) objects, as it never made much sense.
