---
layout: page
title: Software
permalink: /software/
nav: true
nav_order: 4
description: R packages and templates.
---

<div class="pub-list">
  {% for i in site.data.software %}
    {% include software/card.html item=i %}
  {% endfor %}
</div>