---
layout: home
---
<h1>List of Webinars</h1>

<dl>
{% assign sequence = site.webinars | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}


{% assign psize = webinar.presenter-ids | size %}
{% if psize == 1 %}
  {%- assign plabel = "Presenter:" -%}
{% else %}
  {%- assign plabel = "Presenters:" -%}
{% endif %}

{%- assign pstring = "" -%}
{% for pid in webinar.presenter-ids %}
  {% if forloop.index > 1 %}
    {% assign pstring = pstring | append: ", " %}
    {% if forloop.last %}
      {% assign pstring = pstring | append: " and " %}
    {% endif %}
  {% endif %}

  {%- assign p = site.presenters | where: "presenter-id", pid -%}
  {%- capture pafil -%}{{ p[0].firstname }} {{ p[0].lastname }} ({{- p[0].affiliations | array_to_sentence_string | lstrip | rstrip -}}){%- endcapture -%}
  {%- assign pstring = pstring | append: pafil -%}
{% endfor %}

<section style="margin-bottom: 15px">
  <dt>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> ({{ webinar.date | date: "%F" }})
  </dt> 
    {% if pstring %}
	<dd style="margin-left: 30px"><strong>{{ plabel }}</strong> {{ pstring | markdownify | remove: "<p>" | remove: "</p>" | strip }}
      </dd>
    {% endif %}
	<dd style="margin-left: 30px"><strong>Decription:</strong> {{ webinar.content }}</dd>
</section>
{% endfor %}
</dl>
