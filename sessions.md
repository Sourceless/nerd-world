---
layout: default
title: Session Reports
permalink: /sessions/
---

<div class="site-wrapper">
  <h1 style="font-family: 'Cinzel', serif; color: #d4af37; margin-bottom: 0.25em;">Session Reports</h1>
  <p style="color: rgba(244,232,193,0.65); margin-bottom: 2rem; font-family: 'Cinzel', serif; font-size: 0.9rem; letter-spacing: 0.04em;">A record of every adventure in Nerd World</p>

  <div class="sessions-list">
    {% if site.posts.size > 0 %}
      {% for post in site.posts %}
      <div class="session-card">
        <div class="session-title">
          <a href="{{ post.url | relative_url }}">{{ post.title }}</a>
        </div>
        <div class="session-meta">
          <span><span class="meta-label">Date</span> {{ post.date | date: "%B %-d, %Y" }}</span>
          {% if post.dm %}<span><span class="meta-label">DM</span> {{ post.dm }}</span>{% endif %}
          {% if post.players %}<span><span class="meta-label">Players</span> {{ post.players | size }}</span>{% endif %}
          {% if post.xp_awarded %}<span><span class="meta-label">XP</span> {{ post.xp_awarded }}</span>{% endif %}
        </div>
        {% if post.excerpt %}
        <p class="session-excerpt">{{ post.excerpt | strip_html | truncatewords: 40 }}</p>
        {% endif %}
      </div>
      {% endfor %}
    {% else %}
      <div class="sessions-empty">
        <p>No sessions have been posted yet.<br>Check back after Session Zero!</p>
      </div>
    {% endif %}
  </div>
</div>
