---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

<table style="width:100%; border-collapse: collapse; margin-bottom: 1em;">
{% for item in site.data.news %}
  <tr style="border-bottom: 1px solid #e8e8e8;">
    <td style="width:120px; padding:10px 18px 10px 0; vertical-align:top; white-space:nowrap; color:#666; font-weight:bold; font-size:0.88em;">{{ item.date }}</td>
    <td style="padding:10px 0; vertical-align:top; font-size:0.95em; line-height:1.5;">{{ item.content | markdownify }}</td>
  </tr>
{% endfor %}
</table>
