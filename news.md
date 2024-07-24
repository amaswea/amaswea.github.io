---
layout: page
permalink: /news/
title: Media
class: news
---

{:.hidden}
# Media

{% assign media = site.data.news | group_by:"date" %}
{% for article in media %}
{:.news-title}
### {{ article.text }}
{% assign sorted_media = media.items | sort: 'date' | reverse %}
{% for article in sorted_media  %}
  {% include news.html media=media %}
{% endfor %}
{% endfor %}
