---
layout: archive
title: "News"
permalink: /news/
author_profile: true
---

<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@300;400;500;700&family=DM+Mono:wght@400;500&display=swap" rel="stylesheet">

<style>
.news-timeline {
  position: relative;
  margin-top: 1.5rem;
  padding-left: 0;
  font-family: 'DM Sans', sans-serif;
}

.news-year {
  margin: 2.5rem 0 1rem;
  font-family: 'DM Serif Display', serif;
  font-size: 2rem;
  line-height: 1;
  color: #18222d;
}

.news-entry {
  position: relative;
  display: grid;
  grid-template-columns: 108px 1fr;
  column-gap: 1.5rem;
  padding: 0 0 1.75rem;
}

.news-entry:last-child {
  padding-bottom: 0;
}

.news-entry::before {
  content: "";
  position: absolute;
  left: 100px;
  top: 0.4rem;
  bottom: -0.4rem;
  width: 2px;
  background: linear-gradient(180deg, #cfd8df 0%, #e7edf1 100%);
}

.news-entry:last-child::before {
  bottom: 0.7rem;
}

.news-date {
  position: relative;
  z-index: 1;
  font-family: 'DM Mono', monospace;
  font-size: 0.84rem;
  color: #6a7783;
  padding-top: 0.1rem;
}

.news-date::after {
  content: "";
  position: absolute;
  right: -1.03rem;
  top: 0.35rem;
  width: 12px;
  height: 12px;
  border-radius: 999px;
  background: #18222d;
  box-shadow: 0 0 0 5px #f7fafc;
}

.news-card {
  background: linear-gradient(180deg, #ffffff 0%, #f8fbfd 100%);
  border: 1px solid #e2e8ee;
  border-radius: 18px;
  padding: 1rem 1.15rem 1rem 1.2rem;
  box-shadow: 0 10px 30px rgba(22, 35, 48, 0.06);
}

.news-meta {
  display: flex;
  align-items: center;
  gap: 0.65rem;
  flex-wrap: wrap;
  margin-bottom: 0.65rem;
}

.news-badge {
  display: inline-flex;
  align-items: center;
  gap: 0.4rem;
  padding: 0.28rem 0.7rem;
  border-radius: 999px;
  font-size: 0.72rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

.news-badge--preprint {
  background: #e8f7ed;
  color: #177245;
}

.news-badge--conference {
  background: #e8f0ff;
  color: #1f5fd1;
}

.news-badge--poster {
  background: #fff3e5;
  color: #b66700;
}

.news-badge--internship {
  background: #fff0ea;
  color: #c45828;
}

.news-badge--education {
  background: #f1ebff;
  color: #6f3fd1;
}

.news-badge--industry {
  background: #eef7ff;
  color: #1870a8;
}

.news-badge--award {
  background: #fff8dd;
  color: #8d6a00;
}

.news-label {
  font-size: 0.8rem;
  font-weight: 500;
  color: #7b8792;
}

.news-content {
  font-size: 1rem;
  font-weight: 400;
  line-height: 1.75;
  color: #31404c;
}

.news-content p {
  margin: 0;
}

.news-content a {
  color: #18222d;
  text-decoration: underline;
  text-underline-offset: 3px;
}

.news-content strong {
  color: #121a22;
  font-weight: 700;
}

@media (max-width: 700px) {
  .news-year {
    font-size: 1.6rem;
  }

  .news-entry {
    grid-template-columns: 1fr;
    padding-left: 1.5rem;
    row-gap: 0.6rem;
  }

  .news-entry::before {
    left: 0.35rem;
    top: 0.15rem;
    bottom: -0.6rem;
  }

  .news-date {
    padding-top: 0;
    padding-left: 1rem;
  }

  .news-date::after {
    left: -0.02rem;
    right: auto;
    top: 0.2rem;
  }
}
</style>

<div class="news-timeline">
{% assign active_year = "" %}
{% for item in site.data.news %}
  {% assign item_year = item.date | split: " " | last %}
  {% if item_year != active_year %}
    {% assign active_year = item_year %}
    <h2 class="news-year">{{ active_year }}</h2>
  {% endif %}

  {% assign badge_text = "Update" %}
  {% assign badge_class = "conference" %}
  {% assign badge_icon = "📌" %}

  {% if item.label contains "Preprint" %}
    {% assign badge_text = "Preprint" %}
    {% assign badge_class = "preprint" %}
    {% assign badge_icon = "📄" %}
  {% elsif item.label contains "Paper" %}
    {% assign badge_text = "Conference" %}
    {% assign badge_class = "conference" %}
    {% assign badge_icon = "🏆" %}
  {% elsif item.label contains "Poster" %}
    {% assign badge_text = "Poster" %}
    {% assign badge_class = "poster" %}
    {% assign badge_icon = "📌" %}
  {% elsif item.label contains "Internship" %}
    {% assign badge_text = "Internship" %}
    {% assign badge_class = "internship" %}
    {% assign badge_icon = "💼" %}
  {% elsif item.label contains "PhD" or item.label contains "B.Sc." %}
    {% assign badge_text = "Education" %}
    {% assign badge_class = "education" %}
    {% assign badge_icon = "🎓" %}
  {% elsif item.label contains "Award" %}
    {% assign badge_text = "Award" %}
    {% assign badge_class = "award" %}
    {% assign badge_icon = "🏅" %}
  {% elsif item.label contains "DeshiPay" or item.label contains "Ridmik" or item.label contains "Prefeex" or item.label contains "iPay" %}
    {% assign badge_text = "Industry" %}
    {% assign badge_class = "industry" %}
    {% assign badge_icon = "🚀" %}
  {% endif %}

  <article class="news-entry">
    <div class="news-date">{{ item.date }}</div>
    <div class="news-card">
      <div class="news-meta">
        <span class="news-badge news-badge--{{ badge_class }}">{{ badge_icon }} {{ badge_text }}</span>
        <span class="news-label">{{ item.label }}</span>
      </div>
      <div class="news-content">{{ item.content | markdownify }}</div>
    </div>
  </article>
{% endfor %}
</div>
