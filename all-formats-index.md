---
layout: home
---
## List of All Generated Formats, by Webinar

[BSSw Curated Content](hpcbp-webinars-cc.md)

{% assign sequence = site.webinars | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}

{% include upcoming-event event=webinar.date %}
{% include ready-to-advertise webinar=webinar %}
{% include ready-for-event webinar=webinar %}

{% assign be = site.bssw-events | where: "webinar-id", webinar.webinar-id %}
{% assign bed = site.bssw-events-digest | where: "webinar-id", webinar.webinar-id %}
{% assign ipw = site.ipweb-entries | where: "webinar-id", webinar.webinar-id %}
{% assign yt = site.youtube-videos | where: "webinar-id", webinar.webinar-id %}
{% assign ce = site.connection-emails | where: "webinar-id", webinar.webinar-id %}

{{ webinar.webinar-id }}\. **{{ webinar.title }}** ({{ webinar.date | date: "%F" }})

{% include webinar-attributes-table webinar=webinar %}

*Formats* | [Web]({{ site.baseurl }}{{ webinar.url }}) | [BSSw Event]({{ site.baseurl }}{{ be[0].url }}) | [BSSw Digest]({{ site.baseurl }}{{ bed[0].url }}) | [i-p.o WordPress]({{ site.baseurl }}{{ ipw[0].url }})
 | [YouTube]({{ site.baseurl }}{{ yt[0].url }}) | [Connection Email]({{ site.baseurl }}{{ ce[0].url }})

{% endfor %}
