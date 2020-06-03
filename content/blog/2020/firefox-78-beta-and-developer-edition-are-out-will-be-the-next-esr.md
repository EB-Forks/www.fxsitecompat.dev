---
title: "Firefox 78 Beta and Developer Edition are out, will be the next ESR"
date: "2020-06-02T22:30:00-04:00"
---
Mozilla shipped [Firefox 78 Beta and Developer Edition](https://www.mozilla.org/firefox/channel/desktop/) today. We have posted [three site compatibility notes](https://www.fxsitecompat.dev/en-CA/releases/78/) for the forthcoming release, but two are unprefixes, and another one is a rarely used method, so nothing should be affecting your site.

Firefox 78 will be the next [Extended Support Release](https://support.mozilla.org/kb/choosing-firefox-update-channel) (ESR) to be maintained for a year for enterprise users. We’ll create the Firefox 78 ESR Site Compatibility page once it’s out on July 28, at the same time as the regular Rapid Release. The good news is, Firefox engineers are aiming to enable the Service Worker API and push notifications [previously disabled in ESR](https://www.fxsitecompat.dev/en-CA/docs/2019/service-workers-and-push-notifications-are-disabled-on-firefox-68-esr/), which will soon be confirmed.

Some breaking changes are likely to be back with Firefox 79, as society is gradually reopening. The following major changes have been postponed because of the current COVID-19 pandemic:

* [Removing TLS 1.0/1.1 support](https://www.fxsitecompat.dev/en-CA/docs/2020/tls-1-0-1-1-support-has-been-removed/)
* [Removing DTLS 1.0 support from WebRTC](https://www.fxsitecompat.dev/en-CA/docs/2020/dtls-1-0-support-in-webrtc-has-been-removed/)
* [Removing FTP support](https://www.fxsitecompat.dev/en-CA/docs/2020/ftp-support-will-be-removed/)
* [Removing Application Cache storage](https://www.fxsitecompat.dev/en-CA/docs/2020/application-cache-storage-has-been-removed/)
* [Enforcing MIME check for worker scripts](https://www.fxsitecompat.dev/en-CA/docs/2020/worker-scripts-with-wrong-mime-type-will-be-blocked-from-loading-with-worker-or-sharedworker/)
* Making cookies `SameSite=Lax` by default

Also, remember that the [Flash support will be removed](https://www.fxsitecompat.dev/en-CA/docs/2018/flash-plug-in-support-will-be-removed-in-2020/) by the end of the year. Be sure to plan ahead.
