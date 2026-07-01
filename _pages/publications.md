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

.pubs-intro {
  margin: 0 0 2.5rem;
}

.pubs-title {
  margin: 0 0 0.85rem;
  font-family: 'DM Serif Display', serif;
  font-size: 2.1rem;
  line-height: 1.05;
  color: #15212b;
}

.pubs-copy {
  max-width: 760px;
  margin: 0 0 1rem;
  font-size: 1.02rem;
  line-height: 1.8;
  color: #465762;
}

.pubs-scholar {
  display: inline-flex;
  align-items: center;
  gap: 0.45rem;
  padding: 0.7rem 1rem;
  border-radius: 999px;
  background: #eef5fb;
  color: #134b76;
  font-weight: 700;
  text-decoration: none;
}

.pubs-research {
  margin: 2rem 0 0;
}

.pubs-label {
  margin: 0 0 0.85rem;
  font-size: 0.82rem;
  font-weight: 700;
  letter-spacing: 0.08em;
  text-transform: uppercase;
  color: #718290;
}

.pubs-tags {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
}

.pubs-tag {
  display: inline-flex;
  align-items: center;
  padding: 0.5rem 0.85rem;
  border-radius: 999px;
  background: #f4f7f9;
  border: 1px solid #dbe4ea;
  font-size: 0.9rem;
  font-weight: 600;
  color: #334552;
}

.pubs-section {
  margin-top: 3rem;
}

.pubs-section-title {
  margin: 0 0 1.15rem;
  font-family: 'DM Serif Display', serif;
  font-size: 1.7rem;
  color: #15212b;
}

.pubs-grid {
  display: grid;
  gap: 2.2rem;
}

.pub-card {
  display: grid;
  grid-template-columns: 184px minmax(0, 1fr);
  gap: 1.3rem;
  padding: 1.35rem;
  border: 1px solid #dfe7ed;
  border-radius: 26px;
  background: linear-gradient(180deg, #ffffff 0%, #f8fbfd 100%);
  box-shadow: 0 16px 40px rgba(19, 33, 43, 0.08);
  transition: transform 0.2s ease, box-shadow 0.2s ease, border-color 0.2s ease;
}

.pub-card:hover {
  transform: translateY(-3px);
  box-shadow: 0 24px 48px rgba(19, 33, 43, 0.12);
  border-color: #c6d6e2;
}

.pub-card--featured {
  grid-template-columns: 220px minmax(0, 1fr);
  padding: 1.55rem;
}

.pub-visual {
  position: relative;
  overflow: hidden;
  min-height: 220px;
  border-radius: 22px;
  background:
    radial-gradient(circle at top right, rgba(255, 255, 255, 0.18), transparent 35%),
    linear-gradient(160deg, #17384d 0%, #24577a 52%, #3d8d8f 100%);
  color: #fff;
}

.pub-visual::before {
  content: "";
  position: absolute;
  inset: auto -18px 24px auto;
  width: 110px;
  height: 110px;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.08);
}

.pub-visual::after {
  content: "";
  position: absolute;
  left: 18px;
  right: 18px;
  bottom: 18px;
  height: 52px;
  border-radius: 16px;
  background:
    linear-gradient(90deg, rgba(255, 255, 255, 0.16) 0%, rgba(255, 255, 255, 0.04) 100%);
}

.pub-visual-inner {
  position: relative;
  z-index: 1;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  height: 100%;
  padding: 1rem;
}

.pub-featured-chip {
  display: inline-flex;
  align-items: center;
  gap: 0.35rem;
  align-self: flex-start;
  padding: 0.38rem 0.72rem;
  border-radius: 999px;
  background: rgba(255, 255, 255, 0.16);
  font-size: 0.74rem;
  font-weight: 700;
  letter-spacing: 0.04em;
  text-transform: uppercase;
}

.pub-visual-meta {
  display: flex;
  flex-direction: column;
  gap: 0.45rem;
}

.pub-visual-year {
  font-family: 'DM Mono', monospace;
  font-size: 0.88rem;
  color: rgba(255, 255, 255, 0.9);
}

.pub-visual-venue {
  font-size: 1.15rem;
  font-weight: 700;
}

.pub-content {
  min-width: 0;
}

.pub-meta {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  gap: 0.55rem;
  margin-bottom: 0.85rem;
}

.pub-badge {
  display: inline-flex;
  align-items: center;
  padding: 0.36rem 0.72rem;
  border-radius: 999px;
  font-size: 0.78rem;
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
  padding: 0.36rem 0.72rem;
  border-radius: 999px;
  background: #f3f6f8;
  color: #3e5160;
  font-size: 0.8rem;
  font-weight: 700;
}

.pub-year {
  font-family: 'DM Mono', monospace;
  font-size: 0.84rem;
  color: #788692;
}

.pub-title {
  margin: 0 0 0.55rem;
  font-size: 1.65rem;
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
  margin: 0 0 0.8rem;
  font-size: 0.95rem;
  line-height: 1.7;
  color: #5b6b76;
}

.pub-keywords {
  display: flex;
  flex-wrap: wrap;
  gap: 0.55rem;
  margin: 0 0 1rem;
}

.pub-keyword {
  display: inline-flex;
  align-items: center;
  padding: 0.38rem 0.74rem;
  border-radius: 999px;
  background: #f7fafc;
  border: 1px solid #d9e4ec;
  font-size: 0.82rem;
  font-weight: 600;
  color: #415563;
}

.pub-summary {
  margin: 0 0 0.95rem;
  font-size: 1.02rem;
  line-height: 1.82;
  color: #334652;
}

.pub-contribution {
  margin: 0 0 1rem;
  font-size: 0.98rem;
  line-height: 1.75;
  color: #20303a;
}

.pub-contribution strong {
  color: #14212b;
}

.pub-highlights {
  margin: 0 0 1.1rem 1.1rem;
  padding: 0;
  color: #455863;
}

.pub-highlights li {
  margin-bottom: 0.38rem;
  line-height: 1.7;
}

.pub-links {
  display: flex;
  flex-wrap: wrap;
  gap: 0.7rem;
}

.pub-link {
  display: inline-flex;
  align-items: center;
  justify-content: center;
  padding: 0.64rem 0.95rem;
  border-radius: 12px;
  background: #edf4fb;
  border: 1px solid #d6e4f0;
  color: #184a72;
  font-size: 0.92rem;
  font-weight: 700;
  text-decoration: none;
  transition: background 0.18s ease, border-color 0.18s ease, color 0.18s ease;
}

.pub-link:hover {
  background: #dfeefd;
  border-color: #bfd7ee;
  color: #0f3b61;
}

.pub-link--primary {
  background: #17384d;
  border-color: #17384d;
  color: #fff;
}

.pub-link--primary:hover {
  background: #1d4760;
  border-color: #1d4760;
  color: #fff;
}

@media (max-width: 840px) {
  .pub-card,
  .pub-card--featured {
    grid-template-columns: 1fr;
  }

  .pub-visual {
    min-height: 180px;
  }

  .pub-title {
    font-size: 1.4rem;
  }
}
</style>

<div class="pubs-shell">
  <section class="pubs-intro">
    <h2 class="pubs-title">Research at the intersection of decision intelligence, graph learning, and high-performance systems.</h2>
    <p class="pubs-copy">This page highlights work on explainable HPC decision-making, graph-based performance analytics, GPU trace analysis, and scalable anomaly detection. The cards below focus on the strongest takeaways from each paper rather than long abstracts.</p>
    <a class="pubs-scholar" href="https://scholar.google.com/citations?hl=en&user=JKt4eMUAAAAJ">Google Scholar ↗</a>

    <div class="pubs-research">
      <p class="pubs-label">Research Areas</p>
      <div class="pubs-tags">
        <span class="pubs-tag">Decision Intelligence</span>
        <span class="pubs-tag">Graph ML</span>
        <span class="pubs-tag">GPU Performance</span>
        <span class="pubs-tag">Explainable AI</span>
        <span class="pubs-tag">HPC Analytics</span>
      </div>
    </div>
  </section>

  <section class="pubs-section">
    <h3 class="pubs-section-title">Featured Papers</h3>
    <div class="pubs-grid">
      {% for post in site.publications reversed %}
        {% if post.featured %}
          {% assign status_class = post.status | default: "Conference" | downcase %}
          <article class="pub-card pub-card--featured">
            <div class="pub-visual">
              <div class="pub-visual-inner">
                <span class="pub-featured-chip">⭐ Featured</span>
                <div class="pub-visual-meta">
                  <span class="pub-visual-year">{{ post.date | date: "%Y" }}</span>
                  <span class="pub-visual-venue">{{ post.venue_short | default: post.status }}</span>
                </div>
              </div>
            </div>
            <div class="pub-content">
              <div class="pub-meta">
                <span class="pub-badge pub-badge--{{ status_class }}">{{ post.status }}</span>
                <span class="pub-venue-pill">{{ post.venue_short | default: post.venue }}</span>
                <span class="pub-year">{{ post.date | date: "%Y" }}</span>
              </div>

              <h4 class="pub-title"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h4>
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

              <div class="pub-links">
                {% if post.paperurl %}
                  {% if post.paperurl contains "arxiv.org" %}
                    <a class="pub-link pub-link--primary" href="{{ post.paperurl }}">📚 arXiv</a>
                  {% else %}
                    <a class="pub-link pub-link--primary" href="{{ post.paperurl }}">📄 Read Paper</a>
                  {% endif %}
                {% endif %}
                <a class="pub-link" href="{{ base_path }}{{ post.url }}">🔗 Details</a>
              </div>
            </div>
          </article>
        {% endif %}
      {% endfor %}
    </div>
  </section>

  <section class="pubs-section">
    <h3 class="pubs-section-title">Other Publications</h3>
    <div class="pubs-grid">
      {% for post in site.publications reversed %}
        {% unless post.featured %}
          {% assign status_class = post.status | default: "Conference" | downcase %}
          <article class="pub-card">
            <div class="pub-visual">
              <div class="pub-visual-inner">
                <span class="pub-featured-chip">{{ post.status | default: "Publication" }}</span>
                <div class="pub-visual-meta">
                  <span class="pub-visual-year">{{ post.date | date: "%Y" }}</span>
                  <span class="pub-visual-venue">{{ post.venue_short | default: post.venue }}</span>
                </div>
              </div>
            </div>
            <div class="pub-content">
              <div class="pub-meta">
                <span class="pub-badge pub-badge--{{ status_class }}">{{ post.status }}</span>
                <span class="pub-venue-pill">{{ post.venue_short | default: post.venue }}</span>
                <span class="pub-year">{{ post.date | date: "%Y" }}</span>
              </div>

              <h4 class="pub-title"><a href="{{ base_path }}{{ post.url }}">{{ post.title }}</a></h4>
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

              <div class="pub-links">
                {% if post.paperurl %}
                  {% if post.paperurl contains "arxiv.org" %}
                    <a class="pub-link pub-link--primary" href="{{ post.paperurl }}">📚 arXiv</a>
                  {% else %}
                    <a class="pub-link pub-link--primary" href="{{ post.paperurl }}">📄 Read Paper</a>
                  {% endif %}
                {% endif %}
                <a class="pub-link" href="{{ base_path }}{{ post.url }}">🔗 Details</a>
              </div>
            </div>
          </article>
        {% endunless %}
      {% endfor %}
    </div>
  </section>
</div>
