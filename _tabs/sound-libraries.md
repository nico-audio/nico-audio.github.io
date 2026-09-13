---
title: SOUND LIBRARIES
icon: fas fa-stream
order: 5
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
.sl-page{
  --sl-paper: rgb(27, 27, 30);
  --sl-paper-raised: rgb(31, 32, 38);
  --sl-line: rgb(49, 49, 52);
  --sl-ink: #EDEDEC;
  --sl-ink-soft: rgb(165, 166, 168);
  --sl-copper: #D98A4C;
  --sl-copper-dim: #A9714B;
  --sl-mono: 'IBM Plex Mono', monospace;
  --sl-display: 'Space Grotesk', sans-serif;

  max-width: 940px;
  margin: 0 auto;
  padding: 0 32px;
}
.sl-page *{ box-sizing: border-box; }
@media (max-width: 640px){ .sl-page{ padding: 0 20px; } }

.sl-logo-row{ text-align: center; padding: 24px 0 8px; }
.sl-logo-row img{ width: 160px; height: auto; }

.sl-intro{
  max-width: 60ch; margin: 24px auto 56px; text-align: center;
  font-size: 15.5px; color: var(--sl-ink-soft);
}
.sl-intro a{ color: var(--sl-ink); text-decoration: none; border-bottom: 1px solid var(--sl-copper); }
.sl-intro a:hover{ color: var(--sl-copper); }

.sl-grid{
  padding-bottom: 56px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}
@media (max-width: 720px){ .sl-grid{ grid-template-columns: 1fr; } }

.sl-card{
  background: var(--sl-paper-raised);
  border: 1px solid var(--sl-line);
  border-radius: 6px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: border-color 0.2s;
}
.sl-card:hover{ border-color: var(--sl-copper-dim); }

.sl-cover{ aspect-ratio: 1/1; width: 100%; display: block; object-fit: cover; }

.sl-body{ padding: 18px 20px; flex: 1; display: flex; flex-direction: column; gap: 8px; }
.sl-title{
  font-family: var(--sl-display); font-weight: 600; font-size: 15px; margin: 0; color: var(--sl-ink);
  letter-spacing: 0.01em;
}
.sl-specs{
  font-family: var(--sl-mono); font-size: 10.5px; color: var(--sl-copper);
  letter-spacing: 0.02em;
}
.sl-desc{ font-size: 13.5px; color: var(--sl-ink-soft); line-height: 1.5; margin: 0; }

.sl-actions{
  padding: 14px 20px 20px;
  display: flex;
  gap: 10px;
  flex-wrap: wrap;
}
.sl-buy-button{
  flex: 1;
  text-align: center;
  padding: 9px 14px;
  border-radius: 5px;
  background: var(--sl-copper);
  color: var(--sl-paper);
  font-family: var(--sl-mono);
  font-size: 12.5px;
  text-decoration: none;
  font-weight: 500;
  transition: background 0.2s;
}
.sl-buy-button:hover{ background: var(--sl-copper-dim); }
.sl-learn-more{
  flex: 1;
  text-align: center;
  padding: 9px 14px;
  border-radius: 5px;
  border: 1px solid var(--sl-line);
  color: var(--sl-ink-soft);
  font-family: var(--sl-mono);
  font-size: 12.5px;
  text-decoration: none;
  transition: border-color 0.2s, color 0.2s;
}
.sl-learn-more:hover{ border-color: var(--sl-copper); color: var(--sl-copper); }

@media (max-width: 380px){
  .sl-actions{ flex-direction: column; }
}
</style>

<div class="sl-page">

  <div class="sl-logo-row">
    <img src="assets/img/Spectrum-logo.png" alt="Spectrum logo">
  </div>

  <p class="sl-intro">In the last few years I've dedicated a lot of time to collecting, exploring, and working on sounds. Now I want to share some of it — that's why I created <a href="https://spectrumlibraries.com" target="_blank" rel="noopener noreferrer">Spectrum Libraries</a>.</p>

  <div class="sl-grid">
    <div class="sl-card">
      <img class="sl-cover" src="assets/img/Skateboard_thumbnail.png" alt="Skateboard Sound Library cover art">
      <div class="sl-body">
        <p class="sl-specs">96kHz · 24-bit · UCS metadata</p>
        <h4 class="sl-title">SKATEBOARD</h4>
        <p class="sl-desc">100% royalty-free sound library 100% royalty-free sound library recorded across different skateparks.</p>
      </div>
      <div class="sl-actions">
        <a class="gumroad-button sl-buy-button" href="https://spectrumlibraries.gumroad.com/l/skateboard">Buy on Gumroad</a>
        <a class="sl-learn-more" href="https://spectrumlibraries.com/skateboard" target="_blank" rel="noopener">Learn more</a>
      </div>
    </div>
    <div class="sl-card">
      <img class="sl-cover" src="assets/img/Interfaces_thumbnail.png" alt="Interfaces Sound Library">
      <div class="sl-body">
        <p class="sl-specs">96kHz · 24-bit · UCS metadata</p>
        <h4 class="sl-title">INTERFACES</h4>
        <p class="sl-desc">100% royalty-free sound library featuring designed user interface sounds. Includes UCS compliant metadata.</p>
      </div>
      <div class="sl-actions">
        <a class="gumroad-button sl-buy-button" href="https://spectrumlibraries.gumroad.com/l/interfaces">Buy on Gumroad</a>
        <a class="sl-learn-more" href="https://spectrumlibraries.com/interfaces" target="_blank" rel="noopener">Learn more</a>
      </div>
    </div>
    <div class="sl-card">
      <img class="sl-cover" src="assets/img/ShredFX_thumbnail.png" alt="ShredFX cover art">
      <div class="sl-body">
        <p class="sl-specs">96kHz · 24-bit · UCS metadata</p>
        <h4 class="sl-title">SHRED FX</h4>
        <p class="sl-desc">100% royalty-free sound library featuring cloth destruction sounds.</p>
      </div>
      <div class="sl-actions">
        <a class="gumroad-button sl-buy-button" href="https://spectrumlibraries.gumroad.com/l/shredfx">Free on Gumroad</a>
        <a class="sl-learn-more" href="https://spectrumlibraries.com/shred-fx" target="_blank" rel="noopener">Learn more</a>
      </div>
    </div>
  </div>

</div>

<!-- Gumroad overlay script — required for .gumroad-button to open the purchase popup -->
<script src="https://gumroad.com/js/gumroad.js"></script>