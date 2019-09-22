{% for webinar in include.sequence %}

{{ webinar.webinar-id }}\. [**{{ webinar.title }}**]({{ site.baseurl }}{{ webinar.url }}) ({{ webinar.date | date: "%F" }})
{% include webinar-attributes-table webinar=webinar %}
{% endfor %}
