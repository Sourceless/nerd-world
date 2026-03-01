---
layout: home
title: Quick Start
---

<div class="home-hero">
  <h1 class="hero-title">Nerd World</h1>
  <p class="hero-tagline">A West Marches D&amp;D Campaign</p>
  <div class="hero-divider"></div>
</div>

<div class="site-wrapper">
  <div class="home-section">
    <ol class="quickstart-steps">
      <li>
        <div class="step-content">
          <strong>Create your character on D&amp;D Beyond</strong>
          <p>Head to <a href="https://www.dndbeyond.com" target="_blank" rel="noopener">dndbeyond.com</a> and create a Level 1 character. Use the Standard Array for ability scores. Any official sourcebook is fair game. See the <a href="{{ '/characters/' | relative_url }}">Character Creation guide</a> for details.</p>
        </div>
      </li>
      <li>
        <div class="step-content">
          <strong>Show up on the third Saturday</strong>
          <p>Sessions run on the <strong>third Saturday of every month</strong> and last 3–6 hours. No RSVP required — just turn up. The DM announces details in Messenger the week before.</p>
        </div>
      </li>
      <li>
        <div class="step-content">
          <strong>Read the house rules</strong>
          <p>We use a handful of tweaks to keep things flowing at the table. Check the <a href="{{ '/rules/' | relative_url }}">Rules page</a> before your first session — it's a short read.</p>
        </div>
      </li>
      <li>
        <div class="step-content">
          <strong>Consider running a session</strong>
          <p>Anyone can be DM! West Marches runs on volunteer DMs. You don't need to be an expert — a one-room dungeon and a clear goal is enough. The <a href="{{ '/dm-guide/' | relative_url }}">DM Guide</a> walks you through everything.</p>
        </div>
      </li>
    </ol>
  </div>

  <div class="home-section">
    <div class="parchment">
      <h2>About Nerd World</h2>
      <p>Nerd World is a <strong><a href="https://www.youtube.com/watch?v=oGAC-gBoX9k" target="_blank" rel="noopener">West Marches</a></strong> campaign: a shared world with a rotating cast of players and DMs. There is no overarching plot — the players drive the story. Each session is self-contained, so you can join one week and miss the next without losing the thread.</p>
      <p>Your character is a mercenary — an adventurer who takes on jobs for gold. The reason the party comes together each session is the job. What you do with the gold, and the scars, and the stories, is up to you.</p>
      <p>The world itself was built using the <strong><a href="https://thecozyartteacher.com/how-to-make-a-rice-fantasy-map/" target="_blank" rel="noopener">Rice and Dice method</a></strong> — a handful of grains of rice scattered on a map to generate geography at random. Mountains, rivers, settlements, and dungeons emerged from that handful of rice, and adventurers have been exploring the gaps ever since.</p>
      <p>New players are always welcome. All you need is a character and a sense of curiosity.</p>
    </div>
  </div>

  <div class="recent-sessions">
    <h2>Recent Sessions</h2>
    {% if site.posts.size > 0 %}
      {% for post in site.posts limit: 3 %}
      <div class="session-card">
        <div class="session-title"><a href="{{ post.url | relative_url }}">{{ post.title }}</a></div>
        <div class="session-meta">
          <span><span class="meta-label">Date</span> {{ post.date | date: "%B %-d, %Y" }}</span>
          {% if post.dm %}<span><span class="meta-label">DM</span> {{ post.dm }}</span>{% endif %}
          {% if post.players %}<span><span class="meta-label">Players</span> {{ post.players | size }}</span>{% endif %}
        </div>
        {% if post.excerpt %}<p class="session-excerpt">{{ post.excerpt | strip_html | truncatewords: 30 }}</p>{% endif %}
      </div>
      {% endfor %}
      <a href="{{ '/sessions/' | relative_url }}" class="view-all-link">View all sessions &rarr;</a>
    {% else %}
      <p style="color: rgba(244,232,193,0.5); font-style: italic;">No sessions posted yet — check back after Session Zero!</p>
    {% endif %}
  </div>
</div>
