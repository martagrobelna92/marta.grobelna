---
layout: page
permalink: /talks/
title: talks
description: Talks I have given, with slides.
nav: true
nav_order: 3
---

<div class="publications">
<ol class="bibliography">
{% for talk in site.data.talks %}
  <li>
    <div class="row">
      <div class="col col-sm-2 abbr">
        <abbr class="badge rounded w-100">{{ talk.date | date: '%Y' }}</abbr>
      </div>
      <div class="col-sm-8">
        <div class="title">{{ talk.title }}</div>
        <div class="author">{{ talk.type }} · {% if talk.when %}{{ talk.when }}{% else %}{{ talk.date | date: '%-d %B %Y' }}{% endif %}</div>
        <div class="periodical"><em>{{ talk.event }}</em>{% if talk.location %}, {{ talk.location }}{% endif %}</div>
        <div class="links">
          {% if talk.slides %}
            <a href="{{ talk.slides | prepend: '/assets/pdf/slides/' | relative_url }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Slides</a>
          {% endif %}
          {% if talk.paper %}
            <a href="{{ talk.paper }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Paper</a>
          {% endif %}
          {% if talk.video %}
            <a href="{{ talk.video }}" class="btn btn-sm z-depth-0" role="button" target="_blank" rel="noopener noreferrer">Video</a>
          {% endif %}
        </div>
      </div>
    </div>
  </li>
{% endfor %}
</ol>
</div>
