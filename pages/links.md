---
layout: base
permalink: /links
---

<div class="link-circle">
  <li>
      <a href="{{ "/" | relative_url }}" title="Homepage">
        <i class="fas fa-globe"></i>
      </a>
  </li>
{% for link in site.data.header_links %}
  {% if link.show == true %}
    <li>
      <a href="{{link.url}}" title="{{link.title}}" target="_blank">
        <i class="{{link.icon}}"></i>
      </a>
    </li>
  {% endif %}
{% endfor %}
</div>
