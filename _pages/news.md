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
  border: none !important;
  margin-top: 0.5em;
  font-family: 'DM Sans', sans-serif;
}
.news-table tr,
.news-table td,
.news-table th {
  border: none !important;
  border-top: none !important;
  border-bottom: none !important;
  box-shadow: none !important;
}
.news-label {
  width: 160px;
  min-width: 140px;
  padding: 16px 20px 16px 0;
  font-family: 'DM Serif Display', serif;
  font-size: 1em;
  color: #2c2c2c;
  text-align: right;
  line-height: 1.4;
  vertical-align: top;
}
.news-date {
  width: 90px;
  min-width: 80px;
  padding: 18px 18px 16px;
  font-family: 'DM Mono', monospace;
  font-size: 0.88em;
  color: #aaa;
  white-space: nowrap;
  text-align: left;
  vertical-align: top;
}
.news-content {
  padding: 16px 0;
  font-family: 'DM Sans', sans-serif;
  font-size: 1em;
  font-weight: 300;
  line-height: 1.75;
  color: #444;
  vertical-align: top;
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
