---
title: "Stretching MathML operators with STIX General fonts have been deprecated"
date: "2020-06-04T22:11:00-04:00"
categories: ["misc"]
tags: []
releases: ["79"]
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1630935"
      title: "Bug 1630935 - Add use counter and deprecation warning for STIXGeneral fonts"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/ufT7Oc42MEc/discussion"
      title: "Intent to deprecate: stretching MathML operators with STIXGeneral fonts"
---
Starting with Firefox 79, the support for stretching MathML operators using the STIX General fonts is deprecated, and disabled by default in the Nightly channel. According to the intent post, these fonts were a “stopgap solution” for an issue later solved with the OpenType MATH fonts.

The support for the STIX General fonts, deprecated since [Firefox 41](https://www.fxsitecompat.dev/en-CA/docs/2015/mathml-default-font-has-been-changed/), will be removed in the future.
