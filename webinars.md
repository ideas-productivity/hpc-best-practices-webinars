---
layout: home
---
<h1>List of Webinars</h1>

{% for webinar in site.webinars reversed %}
<section>
  <h2>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> 
  </h2> 
  <ul>
	<li><strong>Date:</strong> {{ webinar.date | date: "%F" }}</li>
    <li><strong>Presenter:</strong> {{ webinar.author }}</li>
    <li><strong>Decription:</strong> {{ webinar.content }}</li>
  </ul>
</section>
{% endfor %}
