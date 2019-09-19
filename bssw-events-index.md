---
layout: home
---
<h1>List of BSSw Events</h1>

*Note: these are actually Markdown files, but Jekyll insists on giving
them an html extension.  To see something that will make more sense,
you should "view page source" for these pages in your broswer.  In
many browsers, the shortcut is crtl-u.  Otherwise, it can usually be
found on the context (right-click) menu for the page.*

{% assign sequence = site.bssw-events | sort: "webinar-id" | reverse %}
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
  <p>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> ({{ webinar.date | date: "%F" }})
  </p> 
</section>
{% endfor %}
