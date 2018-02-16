---
# You don't need to edit this file, it's empty on purpose.
# Edit theme's home layout instead if you wanna make some changes
# See: https://jekyllrb.com/docs/themes/#overriding-theme-defaults
layout: home
title: Issues
---

Here you will find all of the back issues of Academic Commons listed in reverse chronological order. While we are in the process of restoring articles, links to issues and articles may at times point to the Internet Archive.

[https://web.archive.org/web/20100726091310/http://www.academiccommons.org/issues](https://web.archive.org/web/20100726091310/http://www.academiccommons.org/issues)

{% for issue in site.issues %}
  <h2><a href="{{ issue.url }}">{{ issue.title }}</a></h2>
  {{ issue.content | strip_html | truncatewords: 100 }}
{% endfor %}
