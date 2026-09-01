---
layout: archive
title: "Teaching"
permalink: /contact/
author_profile: true
---

{% include base_path %}

{% for post in site.teaching reversed %}
  {% include archive-single.html %}
{% endfor %}
