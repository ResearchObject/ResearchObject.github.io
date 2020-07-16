---
layout: page
slug: initiative
title: Related initiatives & resources
---

<div class="alert alert-warning" role="alert">
  <strong>Note</strong>: This list is no longer maintained, but is is provided for archival purposes.
</div>

<ul>
{% assign sorted = (site.initiative | sort: 'title')  %}
{% for x in sorted %}
  <li> 
    <a href="{{ x.url }}">
        {{ x.title }}
    </a>
    —
    <small>{{ x.tags | join: ", " }}</small>
  </li>
{% endfor %}
</ul>
