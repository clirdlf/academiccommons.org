---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: pages
---

Here you will find all of the back pages of Academic Commons listed in reverse chronological order. While we are in the process of restoring articles, links to pages and articles may at times point to the Internet Archive.

[https://web.archive.org/web/20100726091310/http://www.academiccommons.org/pages](https://web.archive.org/web/20100726091310/http://www.academiccommons.org/pages)

{% for page in site.pages %}
  <h2><a href="{{ page.url }}">{{ page.title }}</a></h2>
  {{ page.content | strip_html | truncatewords: 100 }}
{% endfor %}
