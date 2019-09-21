---
layout: home
---
<h2>List of BSSw Events</h2>

*Note: these are actually Markdown files, but Jekyll insists on giving
them an html extension.  To see something that will make more sense,
you should "view page source" for these pages in your broswer.  In
many browsers, the shortcut is crtl-u.  Otherwise, it can usually be
found on the context (right-click) menu for the page.*

{% assign sequence = site.bssw-events | sort: "webinar-id" | reverse %}
{% for webinar in sequence %}



<section style="margin-bottom: 15px">
  <p>{{ webinar.webinar-id }}. 
      <strong><a href="{{ site.baseurl }}{{ webinar.url }}">{{ webinar.title }}</a></strong> ({{ webinar.date | date: "%F" }})
  </p> 
</section>
{% endfor %}
