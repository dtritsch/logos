---
layout: default
title: Monographs
permalink: /monographs/
---

{% if site.monographs.size == 0 %}
<div class="empty-monographs-notice">
<h2>No Monographs</h2>
<p>No monographs have been added yet. Check back soon!</p>
</div>
{% else %}
{% for item in site.monographs %}
<article class="full-monograph-item">
    <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
    <p class="monograph-date"><small>{{ item.date | date: "%B %d, %Y" }}</small></p>
    
    <!-- Renders the full body content of the publication -->
    {{ item.content }}
    
</article>
<hr class="section-divider">
{% endfor %}
{% endif %}