---
# Feel free to add content and custom Front Matter to this file.
# To modify the layout, see https://jekyllrb.com/docs/themes/#overriding-theme-defaults

layout: home
---
{% for webinar in site.webinars reversed %}
<section>
  <h1>{{ webinar.webinar-id }}. 
      <strong>{{ webinar.title }}</strong> 
  </h1> 
  <ul>
	<li><strong>Date:</strong> {{ webinar.date | date: "%F" }}</li>
    <li><strong>Presenter:</strong> {{ webinar.author }}</li>
    <li><strong>Decription:</strong> {{ webinar.content }}</li>
  </ul>
</section>
{% endfor %}
