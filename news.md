---
layout: page
permalink: /news/
title: Media
class: news
---

{:.hidden}
# Media
{% assign sorted_media = site.data.news | sort: 'date' | reverse %}
{% for article in sorted_media %}
{:.news-title}
### {{ article.text }}
  {% include news.html media=article %}
{% endfor %}

