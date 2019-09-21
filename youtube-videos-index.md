---
layout: home
---
<h2>List of YouTube Fragments</h2>

{% assign sequence = site.youtube-videos | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}

<section style="margin-bottom: 15px">
  <p>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> ({{ webinar.date | date: "%F" }})
  </p> 
</section>
{% endfor %}
