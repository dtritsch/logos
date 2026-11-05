---
layout: default
title: Case Studies
permalink: /case-studies/
---

{% if site.case_studies.size == 0 %}
<div class="empty-case-studies-notice">
<h2>No Case Studies</h2>
<p>No publications or entries have been added yet. Check back soon!</p>
</div>
{% else %}
{% for item in site.case_studies %}
<article class="full-case-study-item">
    <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
    <p class="case-study-date"><small>{{ item.date | date: "%B %d, %Y" }}</small></p>
    
    <!-- Renders the full body content of the publication -->
    {{ item.content }}
    
</article>
<hr class="section-divider">
{% endfor %}
{% endif %}