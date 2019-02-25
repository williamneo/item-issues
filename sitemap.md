---
layout: default
permalink: /sitemap.html
title: Sitemap
navigation: hide
---

<ul>
{% for resource in site.data.sitemap %}
{% if page.url != resource.url %}{% unless resource.text contains 'Issues' %}
  <li><a href="{{resource.url}}">{{resource.text}}</a></li>
{% endunless %}{% elsif page.url == resource.url %}
  <li>Sitemap (you are here!)</li>
{% endif %}
{% endfor %}
</ul>

<h2>Issues</h2>
<ul>
{% for resource in site.data.sitemap %}
{% if resource.text contains 'Issues' %}
  <li>
  <a href="{{resource.url}}">{{resource.text}}</a>
  {%- if resource.tags -%}&nbsp;({% include tallytag.html tags=resource.tags %}){%- endif -%}
  </li>
{% endif %}
{% endfor %}
</ul>
