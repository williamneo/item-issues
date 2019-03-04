---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
---

{% assign about =  site.pages | where: 'name', 'about.md' | first %}

# {{ about.title }}
{{ about.content }}

For more info about this page itself, check out the [blog page][blog-link]!

[blog-link]: {{ site.baseurl }}{% link blog.md %}
