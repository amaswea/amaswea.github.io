---
layout: page
permalink: /news/
title: Media
class: news
---

{:.hidden}
# Media
{:.news-title}
### {{ article.text }}
{% assign sorted_news =  site.data.news | sort: 'date' | reverse %}
{% for article in sorted_news  %}
  {% include news.html media=article %}
{% endfor %}