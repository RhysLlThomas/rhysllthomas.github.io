---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
redirect_from:
  - /research/
  - /workingpapers/
  - /workingpapers.html
---

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

<ol class="publication-list" reversed>
{% for post in site.research reversed %}
  <li class="publication">
    {{ post.authors | replace: "Thomas, R.L.", "<strong>Thomas, R.L.</strong>" }} ({{ post.year }}).
    {{ post.title }}
    <em>{{ post.venue }}</em>.
    {% if post.paperurl %}<a href="{{ post.paperurl }}">{{ post.paperurl | remove: "https://doi.org/" | prepend: "doi:" }}</a>{% endif %}
  </li>
{% endfor %}
</ol>
