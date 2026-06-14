---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@300;400;500&family=DM+Mono:wght@400&display=swap" rel="stylesheet">

<style>
.news-table {
  width: 100%;
  border-collapse: collapse;
  margin-top: 0.5em;
  font-family: 'DM Sans', sans-serif;
}
.news-table tr {
  border: none;
  vertical-align: top;
}
.news-label {
  width: 160px;
  min-width: 140px;
  padding: 14px 18px 14px 0;
  font-family: 'DM Serif Display', serif;
  font-size: 0.85em;
  color: #2c2c2c;
  text-align: right;
  line-height: 1.4;
}
.news-date {
  width: 84px;
  min-width: 76px;
  padding: 14px 16px;
  font-family: 'DM Mono', monospace;
  font-size: 0.75em;
  font-weight: 400;
  color: #aaa;
  white-space: nowrap;
  text-align: left;
  padding-top: 16px;
}
.news-content {
  padding: 14px 0;
  font-family: 'DM Sans', sans-serif;
  font-size: 0.9em;
  font-weight: 300;
  line-height: 1.7;
  color: #444;
}
.news-content p {
  margin: 0;
}
.news-content a {
  color: #2c2c2c;
  text-decoration: underline;
  text-underline-offset: 3px;
}
.news-content strong {
  font-weight: 500;
  color: #222;
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
