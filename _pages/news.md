---
layout: archive
title: "✨ News"
permalink: /news/
author_profile: true
---

<style>
.news-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 0.5em;
}
.news-table tr {
  border-bottom: 1px solid #ebebeb;
  vertical-align: top;
}
.news-table tr:last-child {
  border-bottom: none;
}
.news-label {
  width: 160px;
  min-width: 140px;
  padding: 12px 14px 12px 0;
  font-size: 0.82em;
  font-weight: 700;
  color: #333;
  text-align: right;
  line-height: 1.4;
}
.news-date {
  width: 88px;
  min-width: 80px;
  padding: 12px 14px;
  font-size: 0.82em;
  color: #999;
  white-space: nowrap;
  text-align: left;
}
.news-content {
  padding: 12px 0;
  font-size: 0.92em;
  line-height: 1.6;
  color: #333;
}
.news-content p {
  margin: 0;
}
@media (max-width: 600px) {
  .news-label, .news-date {
    display: none;
  }
  .news-content {
    padding: 10px 0;
  }
}
</style>

<table class="news-table">
{% for item in site.data.news %}
  <tr>
    <td class="news-label">{{ item.label }}</td>
    <td class="news-date">{{ item.date }}</td>
    <td class="news-content">{{ item.content | markdownify }}</td>
  </tr>
{% endfor %}
</table>
