---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---
<!-- Fixed: link to googlescholar did not work... author data were added this way -->
{% if page.author and site.data.authors[page.author] %}
  {% assign author = site.data.authors[page.author] %}{% else %}{% assign author = site.author %}
{% endif %}

{% if author.googlescholar %}
  You can also find my articles on <u><a href="{{author.googlescholar}}">my Google Scholar profile</a>.</u>
{% endif %}

{% include base_path %}

<!-- Modification based on Nelle's version in our compbio website -->

<!-- {% for post in site.publications reversed %}
  {% include archive-single.html %}
{% endfor %} -->
