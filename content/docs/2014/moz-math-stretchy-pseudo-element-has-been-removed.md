---
title: "`::-moz-math-stretchy` pseudo-element has been removed"
date: "2014-04-03T19:31:02-04:00"
categories: ["css"]
tags: []
releases: ["31", "31-esr"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1000879"
      title: "Bug 1000879 – Remove the ::-moz-math-stretchy pseudo-element."
supported_tools:
  firefox_extension: true
---
The support for the non-standard `::-moz-math-stretchy` pseudo-element, which allowed authors to specify a [`font-family`](https://developer.mozilla.org/docs/Web/CSS/font-family) to use for stretchy operators, has been removed. A [math font](https://developer.mozilla.org/docs/Mozilla/MathML_Project/Fonts) specified on a [`<math>`](https://developer.mozilla.org/docs/Web/HTML/Element/math) element is now inherited to the child nodes.
