---
layout: home
---
## List of ideas-productivity.org Wordpress Fragments

The main webinar page on i-p.o has two distinct sections.

For the UPCOMING section, webinars should have the UPCOMING and READY-TO-ADVERTISE attributes prior to publication.  This also applies to the Upcoming Events bullet on the main and Events pages of the site.

For the PAST section, webinars should have the PAST attribute.  Eventually, as they acquire the ARTIFACTS attribute, they will need to be updated.

{% assign seq = site.ipweb-entries | sort: "webinar-id" | reverse %}
{% include list-of-pages.md sequence=seq %}
