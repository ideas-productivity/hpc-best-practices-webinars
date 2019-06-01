---
layout: default
---
<table>
  <tr>
    <th>Date</th>
    <th>Title, Presenter(s)</th>
  </tr>

{% for webinar in site.posts %}
  <tr>
    <td>{{ webinar.date | date: "%a %-d %b %Y %-I:%M %P %Z" }}</td>
    <td><em>{{ webinar.title}},</em> {{ webinar.author }}</td>
  </tr>
{% endfor %}
</table>
