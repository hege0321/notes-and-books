---
layout: default
title: Research Notes
permalink: /notes.html
---

# Research Notes

長年累積的觀察筆記,分為兩類:產業觀察(文化內容產業現場)與餐桌與田野(飲食、移民與東南亞)。

{% assign groups = "產業觀察,餐桌與田野" | split: "," %}
{% for g in groups %}
## {{ g }}

{% assign plist = site.categories[g] %}
{% for post in plist %}
- {{ post.date | date: "%Y-%m-%d" }} — [{{ post.title }}]({{ post.url | relative_url }})
{% endfor %}
{% endfor %}
