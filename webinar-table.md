---
layout: default
---
{% assign archive_base = "https://ideas-productivity.org/events/hpc-best-practices-webinars/#webinar" %}
<table>
  <tr>
    <th>No.</th>
    <th>Date</th>
    <th>Title, Presenter(s)</th>
  </tr>

{% for webinar in site.webinars %}
  {% capture seqnum %}{{ webinar.webinar-id | prepend: "00" | slice: -3, 3 }}{% endcapture %}
  <tr>
    <td>{{ webinar.webinar-id }}</td>
    <td>{{ webinar.date | date: "%a %-d %b %Y %-I:%M %P %Z" }}</td>
    <td><em><a href="{{ archive_base }}{{ seqnum }}">{{ webinar.title}}</a>,</em> 
	  {{ webinar.author }}
    </td>
  </tr>
{% endfor %}
</table>
