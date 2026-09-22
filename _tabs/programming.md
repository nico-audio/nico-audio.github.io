---
title: PROGRAMMING
icon: fas fa-stream
order: 3
---

<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
.pr-page{
  --pr-paper: rgb(27, 27, 30);
  --pr-paper-raised: rgb(31, 32, 38);
  --pr-line: rgb(49, 49, 52);
  --pr-ink: #EDEDEC;
  --pr-ink-soft: rgb(165, 166, 168);
  --pr-copper: #D98A4C;
  --pr-copper-dim: #A9714B;
  --pr-mono: 'IBM Plex Mono', monospace;
  --pr-display: 'Space Grotesk', sans-serif;

  max-width: 940px;
  margin: 0 auto;
  padding: 0 20px;
}
.pr-page *{ box-sizing: border-box; }
@media (max-width: 640px){ .pr-page{ padding: 0 20px; } }

.pr-section{ padding: 25px 0; }
.pr-section:first-of-type{ padding-top: 10px; }
.pr-section + .pr-section{ border-top: 1px solid var(--pr-line); }
.pr-section.pr-no-divider{ border-top: none; }

.pr-eyebrow{
  font-family: var(--pr-mono); font-size: 12px; color: var(--pr-copper); margin: 0 0 12px 0;
}
.pr-page h1, .pr-page h2, .pr-page h3{
  font-family: var(--pr-display); font-weight: 600; margin: 0; color: var(--pr-ink);
}
.pr-page h1{ font-size: clamp(28px, 4.5vw, 40px); line-height: 1.1; }
.pr-intro{ margin-top: 16px; max-width: 80ch; font-size: 16px; color: var(--pr-ink-soft); }
.pr-group-title{ font-size: 20px; margin-bottom: 6px; }

/* ===== GRID / CARD ===== */
.pr-grid{
  margin-top: 24px;
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 20px;
}
@media (max-width: 720px){ .pr-grid{ grid-template-columns: 1fr; } }

.pr-card{
  background: var(--pr-paper-raised);
  border: 1px solid var(--pr-line);
  border-radius: 4px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
  transition: border-color 0.2s;
}
.pr-card:hover{ border-color: var(--pr-copper-dim); }

.pr-card-thumb{
  aspect-ratio: 16/9;
  background: repeating-linear-gradient(45deg, rgba(255,255,255,0.02) 0 2px, transparent 2px 14px);
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  border-bottom: 1px solid var(--pr-line);
  display: flex; align-items: center; justify-content: center;
  font-family: var(--pr-mono); font-size: 11px; color: var(--pr-ink-soft);
  text-decoration: none;
}

.pr-card-body{ padding: 18px 20px; flex: 1; display: flex; flex-direction: column; gap: 10px; }

.pr-badge-row{ display: flex; flex-wrap: wrap; gap: 6px; }
.pr-badge{
  font-family: var(--pr-mono); font-size: 10.5px; color: var(--pr-ink-soft);
  border: 1px solid var(--pr-line); padding: 3px 9px; border-radius: 10px;
}
.pr-badge.pr-status{ color: var(--pr-copper); border-color: var(--pr-copper-dim); }

.pr-card-title{ font-size: 16px; }
.pr-card-title a{ color: var(--pr-ink); text-decoration: none; border-bottom: 1px solid transparent; }
.pr-card-title a:hover{ color: var(--pr-copper); border-color: var(--pr-copper); }

.pr-card-text{ font-size: 13.5px; color: var(--pr-ink-soft); line-height: 1.55; }

.pr-card-footer{
  margin-top: auto;
  padding: 14px 20px;
  border-top: 1px solid var(--pr-line);
  display: flex;
  justify-content: flex-end;
  gap: 10px;
}
.pr-icon-link{
  width: 30px; height: 30px;
  border-radius: 50%;
  border: 1px solid var(--pr-line);
  display: flex; align-items: center; justify-content: center;
  color: var(--pr-ink-soft);
  text-decoration: none;
  font-size: 13px;
}
.pr-icon-link:hover{ border-color: var(--pr-copper); color: var(--pr-copper); }

.pr-card-thumb{ cursor: pointer; }

/* ===== LIGHTBOX (click a thumbnail to zoom) ===== */
.pr-lightbox{
  position: fixed;
  inset: 0;
  background: rgba(10, 10, 11, 0.85);
  display: none;
  align-items: center;
  justify-content: center;
  padding: 24px;
  z-index: 1000;
}
.pr-lightbox.is-open{ display: flex; }
.pr-lightbox-inner{
  position: relative;
  width: 100%;
  max-width: 900px;
}
.pr-lightbox-frame{
  width: 100%;
  max-height: 80vh;
  background: var(--pr-paper-raised);
  border: 1px solid var(--pr-line);
  border-radius: 4px;
  overflow: hidden;
  display: flex;
  align-items: center;
  justify-content: center;
}
.pr-lightbox-frame img{
  width: 100%;
  max-height: 80vh;
  object-fit: contain;
  display: block;
}
.pr-lightbox-close{
  position: absolute;
  top: -44px;
  right: 0;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  border: 1px solid var(--pr-line);
  background: var(--pr-paper-raised);
  color: var(--pr-ink);
  font-family: var(--pr-mono);
  font-size: 15px;
  cursor: pointer;
}
.pr-lightbox-close:hover{ border-color: var(--pr-copper); color: var(--pr-copper); }
</style>

<div class="pr-page">
  <!-- AUDIO PROGRAMMING -->
  <div class="pr-section pr-no-divider">
    <p class="pr-eyebrow">PROGRAMMING PROJECTS</p>
    <h2 class="pr-group-title">Audio programming</h2>
    <div class="pr-grid">
      <div class="pr-card">
      <div class="pr-card-thumb" data-full-img="../assets/img/lyredelay_vst_august2026.png" role="button" tabindex="0"
        style="background-image:url('/assets/img/lyredelay_vst_august2026.png')" aria-label="Expand Lyre screenshot"></div>
        <div class="pr-card-body">
          <div class="pr-badge-row">
            <span class="pr-badge pr-status">Work in progress</span>
            <span class="pr-badge">C++</span>
            <span class="pr-badge">JUCE</span>
            <span class="pr-badge">VST Plugin</span>
          </div>
          <h3 class="pr-card-title"><a href="/posts/lyre-vst/">Lyre - Granular Delay VST Plugin</a></h3>
          <p class="pr-card-text">Lyre is a granular delay plugin built with the JUCE framework, designed as a tool for creative, experimental sound design or music. At its core it's a ping-pong delay that incorporates negative feedback and integrated filters, for producing new textures and exploring the sonic possibilities of this kind of system.</p>
        </div>
        <div class="pr-card-footer">
          <a class="pr-icon-link" href="https://github.com/nico-audio/LyreDelayVST" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <div class="pr-card">
        <div class="pr-card-thumb" data-full-img="../assets/img/Post_EasterEgg/Fig1_EasterEgg_patch.png" role="button" tabindex="0"
        style="background-image:url('/assets/img/Post_EasterEgg/Fig1_EasterEgg_patch.png')" aria-label="Easter egg screenshot"></div>
        <div class="pr-card-body">
          <div class="pr-badge-row">
            <span class="pr-badge">Pure Data</span>
            <span class="pr-badge">Sound Design</span>
            <span class="pr-badge">Tooling</span>
          </div>
          <h3 class="pr-card-title"><a href="/posts/easteregg/">Easter Egg Sound Design Tool</a></h3>
          <p class="pr-card-text">A "happy accidents" sound design tool built in Pure Data. It allows for loading a sample, manipulating it through an FX chain, and capturing the output using a buffer.</p>
        </div>
        <div class="pr-card-footer">
          <a class="pr-icon-link" href="https://www.youtube.com/watch?v=Gj6VqbLJr6I" target="_blank" rel="noopener" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
          <a class="pr-icon-link" href="https://github.com/nico-audio/pd-patches/tree/master/easter-egg" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
      <div class="pr-card">
        <div class="pr-card-thumb" data-full-img="../assets/img/Post_DopplerEffect/doppler-unity.gif" role="button" tabindex="0"
        style="background-image:url('/assets/img/Post_DopplerEffect/doppler-unity.gif')" aria-label="Doppler effect demo"></div>
        <div class="pr-card-body">
          <div class="pr-badge-row">
            <span class="pr-badge">Unity</span>
            <span class="pr-badge">C#</span>
            <span class="pr-badge">Game Audio</span>
            <span class="pr-badge">Pure Data</span>
          </div>
          <h3 class="pr-card-title"><a href="/posts/doppler-effect/">The Doppler Effect in Unity and Pure Data</a></h3>
          <p class="pr-card-text">A custom implementation of the Doppler effect in Unity, with a C# script controlling the pitch shift of a moving audio source relative to a listener — applying audio physics for more immersive game environments.</p>
        </div>
        <div class="pr-card-footer">
          <a class="pr-icon-link" href="https://www.youtube.com/watch?v=cUD6vHqMwLU" target="_blank" rel="noopener" aria-label="YouTube"><i class="fab fa-youtube"></i></a>
          <a class="pr-icon-link" href="https://github.com/nico-audio/pd-patches" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
    </div>
  </div>

  <!-- GAME DEVELOPMENT -->
  <div class="pr-section">
    <h2 class="pr-group-title">Game Development</h2>
    <div class="pr-grid">
      <div class="pr-card">
        <div class="pr-card-thumb" data-full-img="../assets/img/gordon-v1.gif" role="button" tabindex="0"
        style="background-image:url('/assets/img/gordon-v1.gif')" aria-label="Gordons-island"></div>
        <div class="pr-card-body">
          <div class="pr-badge-row">
            <span class="pr-badge">C++</span>
            <span class="pr-badge">Raylib</span>
            <span class="pr-badge">Game dev</span>
          </div>
          <h3 class="pr-card-title"><a href="https://github.com/nico-audio/GordonsIsland" target="_blank" rel="noopener">Gordon's Island</a></h3>
          <p class="pr-card-text">A 2D top-down adventure game made with C++ and Raylib.</p>
        </div>
        <div class="pr-card-footer">
          <a class="pr-icon-link" href="https://github.com/nico-audio/GordonsIsland" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
        </div>
      </div>
    </div>
  </div>

  <!-- Lightbox: shared by every project thumbnail -->
  <div class="pr-lightbox" id="prLightbox" aria-hidden="true">
    <div class="pr-lightbox-inner">
      <button type="button" class="pr-lightbox-close" id="prLightboxClose" aria-label="Close">✕</button>
      <div class="pr-lightbox-frame" id="prLightboxFrame"></div>
    </div>
  </div>

</div>

<script>
(function(){
  var lightbox = document.getElementById('prLightbox');
  var frame = document.getElementById('prLightboxFrame');
  var closeBtn = document.getElementById('prLightboxClose');
  var lastOpener = null;

  function openLightbox(src, opener){
    if (!src) return;
    frame.innerHTML = '';
    var img = document.createElement('img');
    img.src = src;
    img.alt = '';
    frame.appendChild(img);
    lightbox.classList.add('is-open');
    lightbox.setAttribute('aria-hidden', 'false');
    lastOpener = opener;
    closeBtn.focus();
  }

  function closeLightbox(){
    lightbox.classList.remove('is-open');
    lightbox.setAttribute('aria-hidden', 'true');
    frame.innerHTML = '';
    if (lastOpener) lastOpener.focus();
  }

  document.querySelectorAll('.pr-page [data-full-img]').forEach(function(thumb){
    thumb.addEventListener('click', function(){
      openLightbox(thumb.getAttribute('data-full-img'), thumb);
    });
    thumb.addEventListener('keydown', function(e){
      if (e.key === 'Enter' || e.key === ' ') {
        e.preventDefault();
        openLightbox(thumb.getAttribute('data-full-img'), thumb);
      }
    });
  });

  closeBtn.addEventListener('click', closeLightbox);
  lightbox.addEventListener('click', function(e){
    if (e.target === lightbox) closeLightbox();
  });
  document.addEventListener('keydown', function(e){
    if (e.key === 'Escape' && lightbox.classList.contains('is-open')) closeLightbox();
  });
})();
</script>