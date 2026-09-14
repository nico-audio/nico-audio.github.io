---
title: Demo
icon: fas fa-headphones
order: 1
---
<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
.sd-showcase{
  --sd-paper: rgb(27, 27, 30);
  --sd-paper-raised: rgb(31, 32, 38);
  --sd-line: rgb(49, 49, 52);
  --sd-ink: #EDEDEC;
  --sd-ink-soft: rgb(165, 166, 168);
  --sd-copper: #D98A4C;
  --sd-copper-dim: #A9714B;
  --sd-mono: 'IBM Plex Mono', monospace;
  --sd-display: 'Space Grotesk', sans-serif;

  position: relative;
  max-width: 980px;
  margin: 0 auto;
  padding: 0 32px;
}
.sd-showcase *{ box-sizing: border-box; }

@media (max-width: 640px){
  .sd-showcase{ padding: 0 20px; }
}
.sd-jack{
  position: absolute;
  left: 8px; width: 9px; height: 9px;
  border-radius: 50%;
  background: var(--sd-paper);
  border: 1.5px solid var(--sd-copper);
  transform: translateX(-50%);
}

.sd-section{
  position: relative;
  padding: 56px 0 56px 48px;
  border-bottom: 1px solid var(--sd-line);
}
@media (max-width: 640px){ .sd-section{ padding-left: 0; } }
.sd-section:last-of-type{ border-bottom: none; }

.sd-eyebrow{
  font-family: var(--sd-mono);
  font-size: 12px;
  color: var(--sd-copper);
  margin: 0 0 12px 0;
}
.sd-showcase h1, .sd-showcase h2{
  font-family: var(--sd-display);
  font-weight: 600;
  margin: 0;
  color: var(--sd-ink);
}
.sd-hero{ padding-top: 40px; }
.sd-hero h1{ font-size: clamp(30px, 4.5vw, 44px); line-height: 1.1; }
.sd-hero-desc{ margin-top: 18px; max-width: 80ch; font-size: 16px; color: var(--sd-ink-soft); text-align: justify; }

.sd-reel-frame{
  margin-top: 32px;
  max-width: 640px;
  margin-left: auto;
  margin-right: auto;
  aspect-ratio: 16/9;
  background: var(--sd-paper-raised);
  background-size: cover;
  background-position: center;
  border: 1px solid var(--sd-line);
  border-radius: 4px;
  display:flex;
  align-items:center;
  justify-content:center;
  cursor: pointer;
  overflow: hidden;
}
.sd-reel-frame iframe{
  width: 100%;
  height: 100%;
  border: 0;
}
.sd-play-btn{
  width: 56px; height: 56px;
  border-radius: 50%;
  border: 1.5px solid var(--sd-copper);
  background: rgba(27,27,30,0.55);
  display:flex; align-items:center; justify-content:center;
  color: var(--sd-copper);
  font-size: 16px;
  flex-shrink: 0;
}
.sd-reel-caption{
  text-align:center; margin-top: 12px;
  font-family: var(--sd-mono); font-size: 12px; color: var(--sd-ink-soft);
}

.sd-grid{
  margin-top: 32px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 20px;
}

@media (max-width: 860px){ .sd-grid{ grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 560px){ .sd-grid{ grid-template-columns: 1fr; } }

.sd-card{
  background: var(--sd-paper-raised);
  border: 1px solid var(--sd-line);
  border-radius: 4px;
  overflow: hidden;
  display: flex;
  flex-direction: column;
}
.sd-card-thumb{
  aspect-ratio: 16/9;
  background: repeating-linear-gradient(45deg, rgba(255,255,255,0.02) 0 2px, transparent 2px 14px);
  background-size: cover;
  background-position: center;
  border-bottom: 1px solid var(--sd-line);
  display:flex; align-items:center; justify-content:center;
  cursor: pointer;
}
.sd-card-thumb .sd-play-btn{ width: 40px; height: 40px; font-size: 12px; }
.sd-card-body{ padding: 14px 16px 16px; display:flex; flex-direction:column; gap:8px; flex:1; }
.sd-card-tag{
  align-self: flex-start;
  font-family: var(--sd-mono); font-size: 11px; color: var(--sd-copper);
  border: 1px solid var(--sd-copper-dim); padding: 3px 9px; border-radius: 10px;
}
.sd-card-title{ font-size: 14px; color: var(--sd-ink); line-height: 1.45; }
.sd-card-link{
  margin-top: auto;
  font-family: var(--sd-mono); font-size: 11.5px; color: var(--sd-ink-soft);
  text-decoration: none; border-bottom: 1px solid var(--sd-line);
  align-self: flex-start; padding-bottom: 1px;
}
.sd-card-link:hover{ color: var(--sd-copper); border-color: var(--sd-copper); }

/* ===== LIGHTBOX (grid thumbnails expand here on click) ===== */
.sd-lightbox{
  position: fixed;
  inset: 0;
  background: rgba(10, 10, 11, 0.85);
  display: none;
  align-items: center;
  justify-content: center;
  padding: 24px;
  z-index: 1000;
}
.sd-lightbox.is-open{ display: flex; }
.sd-lightbox-inner{
  position: relative;
  width: 100%;
  max-width: 900px;
}
.sd-lightbox-frame{
  width: 100%;
  aspect-ratio: 16/9;
  background: var(--sd-paper-raised);
  border: 1px solid var(--sd-line);
  border-radius: 4px;
  overflow: hidden;
}
.sd-lightbox-frame iframe{
  width: 100%;
  height: 100%;
  border: 0;
}
.sd-lightbox-close{
  position: absolute;
  top: -44px;
  right: 0;
  width: 34px;
  height: 34px;
  border-radius: 50%;
  border: 1px solid var(--sd-line);
  background: var(--sd-paper-raised);
  color: var(--sd-ink);
  font-family: var(--sd-mono);
  font-size: 15px;
  cursor: pointer;
}
.sd-lightbox-close:hover{ border-color: var(--sd-copper); color: var(--sd-copper); }
</style>

<div class="sd-showcase">

  <!-- SHOWREEL -->
  <div class="sd-section sd-hero">
    <div class="sd-jack" style="top:40px;"></div>
    <p class="sd-eyebrow">PORTFOLIO · SOUND DESIGN</p>
    <h1>Showreel</h1>
    <p class="sd-hero-desc">This showreel contains some of my work such as the magic sound effects in <b>Grid Force - Mask of the Goddess (Dreamnauts studios)</b> and the splash screen for <b>SGC - Short Games Collection #1 (Nerd Monkeys)</b> and redesigns where I re-create an entire scene from scratch.</p>
    <div class="sd-reel-frame" data-yt-inline="zy9apla4ko4" role="button" tabindex="0" aria-label="Play showreel"
         style="background-image:url('https://i.ytimg.com/vi_webp/zy9apla4ko4/sddefault.webp')">
      <div class="sd-play-btn">▶</div>
    </div>
    <p class="sd-reel-caption">Sound design showreel</p>
  </div>

  <!-- TECHNICAL VIDEOS -->
  <div class="sd-section">
    <div class="sd-jack" style="top:56px;"></div>
    <p class="sd-eyebrow">IMPLEMENTATION</p>
    <h2 style="font-size:24px;">Technical videos</h2>
    <div class="sd-grid">
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="hTh3U1SofZo" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/hTh3U1SofZo/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Unreal Engine 5</span>
          <div class="sd-card-title">Dynamic footstep system implementation using Metasounds</div>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="uZTqMzPiV8M" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/uZTqMzPiV8M/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Unity</span>
          <div class="sd-card-title">Soundscaping using coroutines</div>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="wJS7oHe3OCw" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/wJS7oHe3OCw/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Wwise</span>
          <div class="sd-card-title">Dynamic day/night system controlling ambient sound</div>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="cUD6vHqMwLU" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/cUD6vHqMwLU/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Unity / C#</span>
          <div class="sd-card-title">Doppler effect with custom parameters, driven by a C# script</div>
          <a class="sd-card-link" href="https://nico-audio.github.io/posts/doppler-effect/">Tutorial</a>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="X8SD_jf_PII" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/X8SD_jf_PII/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Pure Data</span>
          <div class="sd-card-title">Doppler effect implementation</div>
          <a class="sd-card-link" href="https://nico-audio.github.io/posts/doppler-effect/">Tutorial</a>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="Gj6VqbLJr6I" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/Gj6VqbLJr6I/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Pure Data</span>
          <div class="sd-card-title">Easter egg - A happy accidents generator for creative sound design</div>
          <a class="sd-card-link" href="https://nico-audio.github.io/posts/easteregg/">Tutorial</a>
        </div>
      </div>
    </div>
  </div>
  <!-- MORE SOUND DESIGN -->
  <div class="sd-section">
    <div class="sd-jack" style="top:56px;"></div>
    <p class="sd-eyebrow">REDESIGNS &amp; ORIGINAL WORK</p>
    <h2 style="font-size:24px;">More sound design</h2>
    <div class="sd-grid">
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="69eluR8comA" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/69eluR8comA/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
        <span class="sd-card-tag">Original work</span>
          <div class="sd-card-title"><b>Splash Screen</b> sound design for Short Games Collection #1 (Nerd Monkeys)</div>
          <a class="sd-card-link" href="https://www.nintendo.com/us/store/products/sgc-short-games-collection-1-switch/">Nintendo Store</a>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="XceLiKuplqI" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/XceLiKuplqI/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
        <span class="sd-card-tag">Original work</span>
          <div class="sd-card-title"><b>Magic spells</b> sound design for Grid Force - Mask of the Goddess</div>
          <a class="sd-card-link" href="https://store.steampowered.com/app/1379960/Grid_Force__Mask_Of_The_Goddess/">Steam</a>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="Tf7n4G2A3Tg" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/Tf7n4G2A3Tg/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Redesign</span>
          <div class="sd-card-title">It Takes Two, by Hazelight Studios</div>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="_5OLb5FeOJE" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/_5OLb5FeOJE/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Redesign</span>
          <div class="sd-card-title"><b>Elements</b> - Airwiggles sound design challenge</div>
          <a class="sd-card-link" href="https://store.steampowered.com/app/1468110/Elements/">Steam</a>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="ShWSV1enQIc" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/ShWSV1enQIc/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Redesign</span>
          <div class="sd-card-title"><b>Machinery</b> sounds made for MTS</div>
        </div>
      </div>
      <div class="sd-card">
        <div class="sd-card-thumb" data-yt-lightbox="ccJ3gb8eM8s" role="button" tabindex="0" aria-label="Expand and play video"
             style="background-image:url('https://img.youtube.com/vi/ccJ3gb8eM8s/hqdefault.jpg')">
          <div class="sd-play-btn">▶</div>
        </div>
        <div class="sd-card-body">
          <span class="sd-card-tag">Redesign</span>
          <div class="sd-card-title"><b>Dig Dig Boom</b>(Airwiggles sound design challenge)</div>
          <a class="sd-card-link" href="https://store.steampowered.com/app/2026040/Dig_Dig_Boom/">Steam</a>
        </div>
      </div>
    </div>
  </div>

  <!-- Lightbox: shared by every grid thumbnail -->
  <div class="sd-lightbox" id="sdLightbox" aria-hidden="true">
    <div class="sd-lightbox-inner">
      <button type="button" class="sd-lightbox-close" id="sdLightboxClose" aria-label="Close video">✕</button>
      <div class="sd-lightbox-frame" id="sdLightboxFrame"></div>
    </div>
  </div>
</div>

<script>
(function(){
  var ID_PLACEHOLDER = 'REPLACE_WITH_VIDEO_ID';

  function buildIframe(id){
    var iframe = document.createElement('iframe');
    iframe.src = 'https://www.youtube-nocookie.com/embed/' + id + '?autoplay=1&rel=0';
    iframe.setAttribute('allow', 'accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share');
    iframe.setAttribute('allowfullscreen', '');
    return iframe;
  }

  /* Hero showreel: plays inline in place, same as before */
  document.querySelectorAll('.sd-showcase [data-yt-inline]').forEach(function(thumb){
    function loadInline(){
      var id = thumb.getAttribute('data-yt-inline');
      if (!id || id === ID_PLACEHOLDER) return;
      thumb.style.backgroundImage = 'none';
      thumb.innerHTML = '';
      thumb.appendChild(buildIframe(id));
    }
    thumb.addEventListener('click', loadInline, { once: true });
    thumb.addEventListener('keydown', function(e){
      if (e.key === 'Enter' || e.key === ' ') { e.preventDefault(); loadInline(); }
    }, { once: true });
  });

  /* Grid thumbnails: expand into a lightbox */
  var lightbox = document.getElementById('sdLightbox');
  var lightboxFrame = document.getElementById('sdLightboxFrame');
  var closeBtn = document.getElementById('sdLightboxClose');
  var lastOpener = null;

  function openLightbox(id, opener){
    if (!id || id === ID_PLACEHOLDER) return;
    lightboxFrame.innerHTML = '';
    lightboxFrame.appendChild(buildIframe(id));
    lightbox.classList.add('is-open');
    lightbox.setAttribute('aria-hidden', 'false');
    lastOpener = opener;
    closeBtn.focus();
  }

  function closeLightbox(){
    lightbox.classList.remove('is-open');
    lightbox.setAttribute('aria-hidden', 'true');
    lightboxFrame.innerHTML = ''; /* removing the iframe stops playback */
    if (lastOpener) lastOpener.focus();
  }

  document.querySelectorAll('.sd-showcase [data-yt-lightbox]').forEach(function(thumb){
    thumb.addEventListener('click', function(){
      openLightbox(thumb.getAttribute('data-yt-lightbox'), thumb);
    });
    thumb.addEventListener('keydown', function(e){
      if (e.key === 'Enter' || e.key === ' ') {
        e.preventDefault();
        openLightbox(thumb.getAttribute('data-yt-lightbox'), thumb);
      }
    });
  });

  closeBtn.addEventListener('click', closeLightbox);
  lightbox.addEventListener('click', function(e){
    if (e.target === lightbox) closeLightbox(); /* click on backdrop, not the video itself */
  });
  document.addEventListener('keydown', function(e){
    if (e.key === 'Escape' && lightbox.classList.contains('is-open')) closeLightbox();
  });
})();
</script>