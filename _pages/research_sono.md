---
layout: archive
title: "Echocardiography"
permalink: /research/sono/
author_profile: true
---

{% include base_path %}

<p class="page__lead">
  Advancing real-time cardiac ultrasound diagnostics through GPU-accelerated speckle tracking, high-frame-rate plane-wave imaging, and deep learning-based automated view classification.
</p>

<!-- Iterates through research items and renders full cards inline -->
{% for post in site.research reversed %}
  {% if post.category == "echo" %}
    {% include research-card.html %}
  {% endif %}
{% endfor %}
