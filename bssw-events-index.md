---
layout: home
---
## List of BSSw Events

*Note: these are actually Markdown files, but Jekyll insists on giving
them an html extension.  To see something that will make more sense,
you should "view page source" for these pages in your broswer.  In
many browsers, the shortcut is crtl-u.  Otherwise, it can usually be
found on the context (right-click) menu for the page.*

BSSw Events should have the UPCOMING and READY-TO-ADVERTISE attributes prior to publication.

{% assign seq = site.bssw-events | sort: "webinar-id" | reverse %}
{% include list-of-pages.md sequence=seq %}
