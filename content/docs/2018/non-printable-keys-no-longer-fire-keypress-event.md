---
title: "Non-printable keys no longer fire `keypress` event"
date: "2018-12-11T10:00:00-05:00"
categories: ["dom"]
tags: []
releases: ["65", "68-esr"]
statuses: "breaking"
references:
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=968056"
      title: "Bug 968056 - keypress event shouldn't be fired for non-printable keys"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1440189"
      title: "Bug 1440189 - Stop dispatching keypress event on web content in Nightly"
    - url: "https://bugzilla.mozilla.org/show_bug.cgi?id=1496288"
      title: "Bug 1496288 - Ship Window.event, keyCode change, and keypress event handling changes"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/wW9el-i5mtA/discussion"
      title: "Intent to stop dispatching \"keypress\" event for non-printable keys and key combinations in Nightly and early Beta"
    - url: "https://groups.google.com/d/topic/mozilla.dev.platform/E8DyIJBhu1g/discussion"
      title: "Intent to ship: stop dispatching \"keypress\" events when pressed key (key combination) does not introduce text input"
aliases:
    - "/en-CA/docs/2018/non-printable-keys-will-soon-stop-firing-keypress-event/"
---
In order to follow the [UI Events spec](https://w3c.github.io/uievents/) and other browsers' behaviour, Firefox will stop dispatching the `keypress` event for non-printable keys and key combinations in the near future.

[Non-printable keys](https://developer.mozilla.org/docs/Web/API/KeyboardEvent/keyCode#Non-printable_keys_(function_keys)) are function keys like Home, End, Tab, Escape, Backspace, Page Down, arrows, etc. Non-printable key combinations include Ctrl+A, Alt+G, Command+Shift+M and so on. Web developers should be using the `keydown` event instead to handle those keys.

An exception is the Enter key; pressing Enter with no modifiers, Shift+Enter or Ctrl+Enter will fire the `keypress` event as before, which is invalid in the current spec but compatible with other browsers.

This change has been made to the Nightly and early Beta/DevEdition channels as of Firefox 60. Other channels will also adopt the standard-compliant behaviour once compatibility issues on major sites are solved. Currently, some keyboard shortcuts on *Gmail*, *Google Docs* and *Google Sheets* are known to be broken.

**Update**: The change, originally requested by Google, has been temporarily [backed out](https://bugzilla.mozilla.org/show_bug.cgi?id=1443117) to give Google engineers time to fix the issue in their apps.

**Update 2**: This change has been landed again at Firefox 61 Nightly but disabled for now on *Gmail*, *Google Docs*, *Google Sheets* and *Google Slides* to avoid any breakage.

**Update 3**: *Dropbox Paper*, *Google Hangouts*, *Google Inbox*, *Google Keep* and *Remember The Milk* as well as major public *Etherpad* instances have also been added to the blacklist so those developers have extra time to fix the issue.

If you're a developer of one of those apps who would like to test the new behaviour, you have to override the blacklist with the browser's configuration editor: open [`about:config`](https://support.mozilla.org/kb/about-config-editor-firefox) in Firefox, search `dom.keyboardevent.keypress.hack.dispatch_non_printable_keys`, click on it, empty the value, then click OK.

**Update 4**: This change has been enabled on all the channels as of Firefox 65. All the major site issues have been fixed at their side, and the blacklist is now empty.
