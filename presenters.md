---
layout: home
---
## List of Presenters

<dl>
{% for presenter in site.presenters %}
<section style="margin-bottom: 15px">
  <dt>
    <a href="{{ site.baseurl }}{{ presenter.url }}">
  	  <strong>{{ presenter.firstname }} {{ presenter.lastname }},</strong>
	</a>
    {% if presenter.affiliations %}
      {{ presenter.affiliations | array_to_sentence_string | markdownify |
          remove: "<p>" | remove: "</p>" }}
    {% endif %}
  </dt> 

{% assign w = site.webinars | where: "presenter-ids", presenter.presenter-id | sort: "webinar-id" | reverse %}
  {% if w %}
    {% for w2 in w %}
      <dd style="margin-left: 30px">{{ w2.webinar-id }}. 
        <strong><a href="{{ site.baseurl }}{{ w2.url }}">{{ w2.title }}</a></strong> ({{ w2.date | date: "%F" }})
      </dd>
    {% endfor %}
  {% endif %}

</section>
{% endfor %}
</dl>
