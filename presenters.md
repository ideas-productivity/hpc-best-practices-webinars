---
layout: home
---
<h2>List of Presenters</h2>

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
  <dd style="margin-left: 30px">Webinars</dd>
</section>
{% endfor %}
</dl>
