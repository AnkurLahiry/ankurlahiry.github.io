---
layout: archive
title: "Publications"
permalink: /publications/
author_profile: true
---

{% include base_path %}

<link href="https://fonts.googleapis.com/css2?family=DM+Serif+Display&family=DM+Sans:wght@400;500;700&family=DM+Mono:wght@500&display=swap" rel="stylesheet">

<style>
.pubs-shell {
  font-family: 'DM Sans', sans-serif;
  color: #1b2730;
}

.pubs-section {
  margin-top: 2rem;
}

.pubs-grid {
  display: grid;
  gap: 1.35rem;
}

.pub-card {
  display: block;
  padding: 1rem;
  border: 1px solid #dfe7ed;
  border-radius: 22px;
  background: linear-gradient(180deg, #ffffff 0%, #f8fbfd 100%);
  box-shadow: 0 16px 40px rgba(19, 33, 43, 0.08);
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
}

.pub-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 24px 48px rgba(19, 33, 43, 0.12);
  border-color: #c6d6e2;
}

.pub-content {
  min-width: 0;
}

.pub-meta {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.45rem;
  margin-bottom: 0.7rem;
}

.pub-badge {
  display: inline-flex;
  align-items: center;
  padding: 0.3rem 0.62rem;
  border-radius: 999px;
  font-size: 0.66rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

.pub-badge--preprint {
  background: #e8f7ed;
  color: #177245;
}

.pub-badge--conference {
  background: #e8f0ff;
  color: #1f5fd1;
}

.pub-badge--research-paper {
  background: #e8f0ff;
  color: #1f5fd1;
}

.pub-badge--workshop {
  background: #fff3e5;
  color: #ad6500;
}

.pub-badge--poster {
  background: #fff1e8;
  color: #ba5a27;
}

.pub-badge--journal {
  background: #efeaff;
  color: #6b40cc;
}

.pub-venue-pill {
  display: inline-flex;
  align-items: center;
  padding: 0.3rem 0.62rem;
  border-radius: 999px;
  background: #f3f6f8;
  color: #3e5160;
  font-size: 0.7rem;
  font-weight: 700;
}

.pub-year {
  font-family: 'DM Mono', monospace;
  font-size: 0.72rem;
  color: #788692;
}

.pub-title {
  margin: 0 0 0.45rem;
  font-size: 1.22rem;
  line-height: 1.22;
  font-weight: 700;
}

.pub-title a {
  color: #14212b;
  text-decoration: none;
  transition: color 0.18s ease;
}

.pub-card:hover .pub-title a {
  color: #1d5cc6;
}

.pub-authors {
  margin: 0 0 0.65rem;
  font-size: 0.82rem;
  line-height: 1.6;
  color: #5b6b76;
}

.pub-keywords {
  display: flex;
  flex-wrap: wrap;
  gap: 0.45rem;
  margin: 0 0 0.8rem;
}

.pub-keyword {
  display: inline-flex;
  align-items: center;
  padding: 0.32rem 0.62rem;
  border-radius: 999px;
  background: #f7fafc;
  border: 1px solid #d9e4ec;
  font-size: 0.72rem;
  font-weight: 600;
  color: #415563;
}

.pub-summary {
  margin: 0 0 0.8rem;
  font-size: 0.88rem;
  line-height: 1.62;
  color: #334652;
}

.pub-contribution {
  margin: 0 0 0.85rem;
  font-size: 0.86rem;
  line-height: 1.58;
  color: #20303a;
}

.pub-contribution strong {
  color: #14212b;
}

.pub-highlights {
  margin: 0 0 0.95rem 1rem;
  padding: 0;
  color: #455863;
}

.pub-highlights li {
  margin-bottom: 0.28rem;
  line-height: 1.55;
  font-size: 0.83rem;
}

@media (max-width: 840px) {
  .pub-title {
    font-size: 1.1rem;
  }
}
</style>

<div class="pubs-shell">
  <section class="pubs-section">
    <div class="pubs-grid">
      {% for post in site.publications reversed %}
        {% assign status_class = post.status | default: "Research Paper" | downcase | replace: " ", "-" %}
        <article class="pub-card">
          <div class="pub-content">
            <div class="pub-meta">
              <span class="pub-badge pub-badge--{{ status_class }}">{{ post.status }}</span>
              <span class="pub-venue-pill">{{ post.venue_short | default: post.venue }}</span>
              <span class="pub-year">{{ post.date | date: "%Y" }}</span>
            </div>

            <h4 class="pub-title"><a href="{{ post.paperurl | default: base_path | append: post.url }}">{{ post.title }}</a></h4>
            {% if post.authors %}<p class="pub-authors">{{ post.authors }}</p>{% endif %}

            {% if post.keywords %}
              <div class="pub-keywords">
                {% for keyword in post.keywords %}
                  <span class="pub-keyword">{{ keyword }}</span>
                {% endfor %}
              </div>
            {% endif %}

            {% if post.summary %}<p class="pub-summary">{{ post.summary }}</p>{% endif %}
            {% if post.key_contribution %}<p class="pub-contribution"><strong>Key Contribution:</strong> {{ post.key_contribution }}</p>{% endif %}

            {% if post.highlights %}
              <ul class="pub-highlights">
                {% for item in post.highlights %}
                  <li>{{ item }}</li>
                {% endfor %}
              </ul>
            {% endif %}
          </div>
        </article>
      {% endfor %}
    </div>
  </section>
</div>
