---
layout: default
title: Reading Vault
permalink: /reading-vault/
---

{% if site.reading_vault.size == 0 %}
<div class="empty-vault-notice">
  <h2>Vault is Currently Empty</h2>
  <p>No publications or entries have been added to this vault yet. Check back soon!</p>
</div>
{% else %}
{% for item in site.reading_vault %}
<article class="full-vault-item">
  <h2><a href="{{ item.url | relative_url }}">{{ item.title }}</a></h2>
  <p class="vault-date"><small>{{ item.date | date: "%B %d, %Y" }}</small></p>
  
  <!-- Renders the full body content of the publication -->
  {{ item.content }}
  
</article>
<hr class="section-divider">
{% endfor %}
{% endif %}