---
layout: default
redirect_from: /fixes/
---
{% for fix in site.fixed reversed %}
### {{fix.date | date: "%b %d %Y" }}
{{fix.content}}
{% endfor %}