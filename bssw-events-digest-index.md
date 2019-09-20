---
layout: home
---
<h1>List of BSSw Event Digest Entries</h1>

{% assign sequence = site.bssw-events-digest | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}

<section style="margin-bottom: 15px">
  <p>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> ({{ webinar.date | date: "%F" }})
  </p> 
</section>
{% endfor %}
