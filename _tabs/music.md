---
#layout: tags
title: Music
icon: fas fa-tag
order: 5
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
.op-page{
  --op-paper: rgb(27, 27, 30);
  --op-paper-raised: rgb(31, 32, 38);
  --op-line: rgb(49, 49, 52);
  --op-ink: #EDEDEC;
  --op-ink-soft: rgb(165, 166, 168);
  --op-copper: #D98A4C;
  --op-mono: 'IBM Plex Mono', monospace;
  --op-display: 'Space Grotesk', sans-serif;

  max-width: 760px;
  margin: 0 auto;
  padding: 0 32px;
}
.op-page *{ box-sizing: border-box; }
@media (max-width: 640px){ .op-page{ padding: 0 20px; } }

.op-eyebrow{
  font-family: var(--op-mono); font-size: 12px; color: var(--op-copper); margin: 0 0 12px 0;
}
.op-intro{
  margin: 0 0 32px 0; max-width: 80ch; font-size: 15.5px; color: var(--op-ink-soft);
}

.op-player-frame{
  background: var(--op-paper-raised);
  border: 1px solid var(--op-line);
  border-radius: 6px;
  padding: 16px;
  padding-bottom: 40px;
}
.op-player-frame iframe{
  display: block;
  width: 100%;
  border: 0;
  border-radius: 4px;
}
</style>

<div class="op-page">

  <p class="op-eyebrow">MUSIC</p>
  <p class="op-intro">Here you can find some older musical projects from 2009 to 2019, before I started working in game development.</p>

  <div class="op-player-frame">
    <iframe width="100%" height="450" scrolling="no" frameborder="no" allow="autoplay" src="https://w.soundcloud.com/player/?url=https%3A//api.soundcloud.com/users/271245&color=%23262725&auto_play=false&hide_related=false&show_comments=true&show_user=true&show_reposts=false&show_teaser=true"></iframe>
  </div>

</div>