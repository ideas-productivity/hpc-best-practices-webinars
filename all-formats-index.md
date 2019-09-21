---
layout: home
---
## List of All Generated Formats, by Webinar

[BSSw Curated Content](hpcbp-webinars-cc.md)

{% assign sequence = site.webinars | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}

{% assign be = site.bssw-events | where: "webinar-id", webinar.webinar-id %}
{% assign bed = site.bssw-events-digest | where: "webinar-id", webinar.webinar-id %}
{% assign ipw = site.ipweb-entries | where: "webinar-id", webinar.webinar-id %}
{% assign yt = site.youtube-videos | where: "webinar-id", webinar.webinar-id %}
{% assign ce = site.connection-emails | where: "webinar-id", webinar.webinar-id %}

{{ webinar.webinar-id }}\. **{{ webinar.title }}** ({{ webinar.date | date: "%F" }})
  - [Web]({{ site.baseurl }}{{ webinar.url }})
  - [BSSw Event]({{ site.baseurl }}{{ be[0].url }})
  - [BSSw Digest Entry]({{ site.baseurl }}{{ bed[0].url }})
  - [ideas-productivity.org Wordpress fragments]({{ site.baseurl }}{{ ipw[0].url }})
  - [YouTube fragments]({{ site.baseurl }}{{ yt[0].url }})
  - [Connection Information Email]({{ site.baseurl }}{{ ce[0].url }})
  
{% endfor %}
