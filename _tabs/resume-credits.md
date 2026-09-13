---
title: RESUME & CREDITS
icon: fas fa-info-circle
order: 6
---


<link rel="preconnect" href="https://fonts.googleapis.com">
<link href="https://fonts.googleapis.com/css2?family=Space+Grotesk:wght@400;500;600;700&family=IBM+Plex+Mono:wght@400;500&family=IBM+Plex+Sans:wght@400;500&display=swap" rel="stylesheet">

<style>
.rc-page{
  --rc-paper: rgb(27, 27, 30);
  --rc-paper-raised: rgb(31, 32, 38);
  --rc-line: rgb(49, 49, 52);
  --rc-ink: #EDEDEC;
  --rc-ink-soft: rgb(165, 166, 168);
  --rc-copper: #D98A4C;
  --rc-copper-dim: #A9714B;
  --rc-mono: 'IBM Plex Mono', monospace;
  --rc-display: 'Space Grotesk', sans-serif;

  max-width: 900px;
  margin: 0 auto;
  padding: 0 32px;
}
.rc-page *{ box-sizing: border-box; }
@media (max-width: 640px){ .rc-page{ padding: 0 20px; } }

.rc-section{
  padding: 26px 0;
}
.rc-section:last-of-type{ border-bottom: none; }

.rc-eyebrow{
  font-family: var(--rc-mono);
  font-size: 12px;
  color: var(--rc-copper);
  margin: 0 0 12px 0;
}
.rc-page h1, .rc-page h2{
  font-family: var(--rc-display);
  font-weight: 600;
  margin: 0;
  color: var(--rc-ink);
}

/* ===== CAROUSEL ===== */
.rc-carousel{ margin-top: 32px; }
.rc-carousel-main{
  position: relative;
  aspect-ratio: 16/9;
  background: var(--rc-paper-raised);
  border: 1px solid var(--rc-line);
  border-radius: 4px;
  overflow: hidden;
}
.rc-carousel-slide{
  position: absolute;
  inset: 0;
  display: none;
  align-items: center;
  justify-content: center;
  background: repeating-linear-gradient(45deg, rgba(255,255,255,0.02) 0 2px, transparent 2px 14px);
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  font-family: var(--rc-mono);
  font-size: 12px;
  color: var(--rc-ink-soft);
  text-decoration: none;
}
.rc-carousel-slide.is-active{ display: flex; }
.rc-carousel-slide:hover{ color: var(--rc-copper); }
.rc-carousel-arrow{
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  width: 36px; height: 36px;
  border-radius: 50%;
  background: rgba(27,27,30,0.7);
  border: 1px solid var(--rc-line);
  color: var(--rc-ink);
  display: flex; align-items:center; justify-content:center;
  cursor: pointer;
  font-size: 14px;
  user-select: none;
  z-index: 2;
}
.rc-carousel-arrow:hover{ border-color: var(--rc-copper); color: var(--rc-copper); }
.rc-carousel-arrow.prev{ left: 12px; }
.rc-carousel-arrow.next{ right: 12px; }
.rc-carousel-thumbs{
  display: flex;
  gap: 10px;
  margin-top: 12px;
  justify-content: center;
}
.rc-carousel-thumb{
  width: 72px;
  aspect-ratio: 16/9;
  background: repeating-linear-gradient(45deg, rgba(255,255,255,0.02) 0 2px, transparent 2px 14px);
  background-size: contain;
  background-position: center;
  background-repeat: no-repeat;
  border: 1px solid var(--rc-line);
  border-radius: 3px;
  cursor: pointer;
  opacity: 0.5;
  transition: opacity 0.2s, border-color 0.2s;
}
.rc-carousel-thumb.is-active{ opacity: 1; border-color: var(--rc-copper); }

/* ===== RELEASED TITLES ===== */
.rc-credit-list{ margin-top: 28px; display: flex; flex-direction: column; gap: 22px; }
.rc-credit-item{ display: grid; grid-template-columns: 64px 1fr; gap: 18px; }
@media (max-width: 520px){ .rc-credit-item{ grid-template-columns: 1fr; gap: 6px; } }
.rc-credit-year{ font-family: var(--rc-mono); font-size: 13px; color: var(--rc-copper); padding-top: 3px; }
.rc-credit-body{ border-bottom: 1px solid var(--rc-line); padding-bottom: 18px; }
.rc-credit-item:last-child .rc-credit-body{ border-bottom: none; padding-bottom: 0; }
.rc-credit-title{ font-size: 15.5px; color: var(--rc-ink); }
.rc-credit-title a{ color: var(--rc-ink); text-decoration: none; border-bottom: 1px solid var(--rc-copper); }
.rc-credit-title a:hover{ color: var(--rc-copper); }
.rc-credit-role{
  display: inline-block;
  margin-top: 6px;
  font-family: var(--rc-mono);
  font-size: 11px;
  color: var(--rc-copper);
  border: 1px solid var(--rc-copper-dim);
  padding: 2px 9px;
  border-radius: 10px;
}
.rc-credit-desc{ margin-top: 8px; font-size: 14px; color: var(--rc-ink-soft); max-width: 60ch; }

/* ===== SKILL / TAG GRIDS ===== */
.rc-skill-grid{
  margin-top: 28px;
  display: grid;
  grid-template-columns: repeat(3, 1fr);
  gap: 12px;
}
@media (max-width: 640px){ .rc-skill-grid{ grid-template-columns: repeat(2, 1fr); } }
@media (max-width: 420px){ .rc-skill-grid{ grid-template-columns: 1fr; } }
.rc-skill-card{
  background: var(--rc-paper-raised);
  border: 1px solid var(--rc-line);
  border-radius: 4px;
  padding: 12px 14px;
}
.rc-skill-name{ font-size: 14px; color: var(--rc-ink); }
.rc-skill-level{ margin-top: 4px; font-family: var(--rc-mono); font-size: 11px; color: var(--rc-ink-soft); }

.rc-tag-cloud{ margin-top: 28px; display: flex; flex-wrap: wrap; gap: 10px; }
.rc-tag-pill{
  font-family: var(--rc-mono);
  font-size: 12.5px;
  color: var(--rc-ink-soft);
  border: 1px solid var(--rc-line);
  padding: 6px 13px;
  border-radius: 16px;
}

/* ===== SIMPLE LISTS (certifications, education) ===== */
.rc-simple-list{ margin-top: 28px; list-style: none; padding: 0; display: flex; flex-direction: column; }
.rc-simple-list li{
  display: flex;
  gap: 16px;
  padding: 11px 0;
  border-bottom: 1px solid var(--rc-line);
  font-size: 14.5px;
  color: var(--rc-ink-soft);
}
.rc-simple-list li:last-child{ border-bottom: none; }
.rc-simple-list .rc-yr{
  font-family: var(--rc-mono);
  font-size: 12.5px;
  color: var(--rc-copper);
  flex-shrink: 0;
  width: 44px;
}
.rc-simple-list strong{ color: var(--rc-ink); font-weight: 500; }

/* ===== SOCIAL / CONTACT ===== */
.rc-social-row{ margin-top: 28px; display: flex; gap: 16px; }
.rc-social-link{
  width: 38px; height: 38px;
  border-radius: 50%;
  border: 1px solid var(--rc-line);
  display: flex; align-items:center; justify-content:center;
  color: var(--rc-ink-soft);
  text-decoration: none;
  font-size: 15px;
}
.rc-social-link:hover{ border-color: var(--rc-copper); color: var(--rc-copper); }
</style>

<div class="rc-page">

  <!-- CAROUSEL -->
  <div class="rc-section" id="rc-showreel">
    <div class="rc-carousel">
      <div class="rc-carousel-main" id="rcCarouselMain">
        <a class="rc-carousel-slide" href="https://www.youtube.com/watch?v=FalEcRLGzhY" target="_blank" rel="noopener"
          style="background-image:url('https://user-images.githubusercontent.com/110834120/249539750-8d4530ae-d3bf-4412-982b-44efe86eed53.png');" aria-label="Grid Force — watch on YouTube"></a>
        <a class="rc-carousel-slide" href="https://www.youtube.com/watch?v=qfJY5a9Vzz8" target="_blank" rel="noopener"                      
          style="background-image:url('https://github.com/nico-audio/nico-audio.github.io/assets/110834120/68df4e8d-e827-4688-9bca-12cadc3d7e85');" aria-label="SGC — watch on YouTube"></a>
        <a class="rc-carousel-slide"               
          style="background-image:url('https://github.com/nico-audio/nico-audio.github.io/assets/110834120/a076e0c1-7e89-40b3-a5ba-f23488cffae4');" aria-label="Fracture — watch on YouTube"></a>
        <button class="rc-carousel-arrow prev" onclick="rcPlusSlides(-1)" aria-label="Previous">‹</button>
        <button class="rc-carousel-arrow next" onclick="rcPlusSlides(1)" aria-label="Next">›</button>
      </div>
      <div class="rc-carousel-thumbs" id="rcCarouselThumbs">
        <div class="rc-carousel-thumb is-active" onclick="rcCurrentSlide(1)"
          style ="background-image:url('https://user-images.githubusercontent.com/110834120/249539750-8d4530ae-d3bf-4412-982b-44efe86eed53.png');">
        </div>
        <div class="rc-carousel-thumb" onclick="rcCurrentSlide(2)"          
          style ="background-image:url('https://github.com/nico-audio/nico-audio.github.io/assets/110834120/68df4e8d-e827-4688-9bca-12cadc3d7e85');">
        </div>
        <div class="rc-carousel-thumb" onclick="rcCurrentSlide(3)"
          style ="background-image:url('https://github.com/nico-audio/nico-audio.github.io/assets/110834120/a076e0c1-7e89-40b3-a5ba-f23488cffae4');">
        </div>
      </div>
    </div>
  </div>

  <!-- RELEASED TITLES -->
  <div class="rc-section" id="rc-titles">
    <p class="rc-eyebrow">CREDITS</p>
    <h2 style="font-size:22px;">Released titles</h2>
    <div class="rc-credit-list">
      <div class="rc-credit-item">
        <div class="rc-credit-year">2021</div>
        <div class="rc-credit-body">
          <div class="rc-credit-title"><a href="https://store.steampowered.com/app/1379960/Grid_Force__Mask_Of_The_Goddess/" target="_blank" rel="noopener">Grid Force - Mask of the Goddess</a> — Dreamnauts studios</div>
          <span class="rc-credit-role">Sound designer</span>
          <p class="rc-credit-desc">Designed elemental magic for characters in this game and composed a leitmotif.</p>
        </div>
      </div>
      <div class="rc-credit-item">
        <div class="rc-credit-year">2021</div>
        <div class="rc-credit-body">
          <div class="rc-credit-title"><a href="https://www.nintendo.com/store/products/sgc-short-games-collection-1-switch/" target="_blank" rel="noopener">SGC - Short Games Collection #1</a> — Nerd Monkeys</div>
          <span class="rc-credit-role">Sound designer</span>
          <p class="rc-credit-desc">Designed the splash screen sound that opens the game.</p>
        </div>
      </div>
      <div class="rc-credit-item">
        <div class="rc-credit-year">2020</div>
        <div class="rc-credit-body">
          <div class="rc-credit-title"><a href="https://www.legendsoflearning.com/math-basecamp/" target="_blank" rel="noopener">Fracture</a> — StaalMedia, Nerd Monkeys</div>
          <span class="rc-credit-role">Audio designer</span>
          <p class="rc-credit-desc">Part of the development team, designing sounds and helping with audio implementation on this educational math game.</p>
        </div>
      </div>
    </div>
  </div>

  <!-- LANGUAGE SKILLS -->
  <div class="rc-section" id="rc-languages">
    <h2 style="font-size:22px;">Language skills</h2>
    <div class="rc-skill-grid">
      <div class="rc-skill-card"><div class="rc-skill-name">Portuguese</div><div class="rc-skill-level">Native</div></div>
      <div class="rc-skill-card"><div class="rc-skill-name">English</div><div class="rc-skill-level">Proficient</div></div>
      <div class="rc-skill-card"><div class="rc-skill-name">Spanish</div><div class="rc-skill-level">Intermediate</div></div>
      <div class="rc-skill-card"><div class="rc-skill-name">Catalan</div><div class="rc-skill-level">Intermediate</div></div>
    </div>
  </div>

  <!-- PROGRAMMING / SOFTWARE SKILLS -->
  <div class="rc-section" id="rc-skills">
    <h2 style="font-size:22px;">Programming &amp; software skills</h2>
    <div class="rc-tag-cloud">
      <span class="rc-tag-pill">Wwise</span>
      <span class="rc-tag-pill">Unreal Engine</span>
      <span class="rc-tag-pill">Unity Engine</span>
      <span class="rc-tag-pill">C#</span>
      <span class="rc-tag-pill">C++</span>
      <span class="rc-tag-pill">Pure Data</span>
      <span class="rc-tag-pill">Unreal Blueprints</span>
      <span class="rc-tag-pill">JUCE</span>
      <span class="rc-tag-pill">Reaper</span>
      <span class="rc-tag-pill">Ableton Live</span>
    </div>
  </div>

  <!-- CERTIFICATIONS -->
  <div class="rc-section" id="rc-certs">
    <p class="rc-eyebrow">ONGOING LEARNING</p>
    <h2 style="font-size:22px;">Certifications &amp; training</h2>
    <ul class="rc-simple-list">
      <li><span class="rc-yr">2025</span><span><strong>Gamedev.tv - C++ Fundamentals</strong></span></li>
      <li><span class="rc-yr">2023</span><span><strong>Audiokinetic - Wwise 251 - Performance Optimization & Mobile Considerations</strong></span></li>
      <li><span class="rc-yr">2022</span><span><strong>Audiokinetic - Wwise 201 - Interactive Music</strong></span></li>
      <li><span class="rc-yr">2022</span><span><strong>Gamedev.tv - Complete C# Unity Game Developer 2D Online Course</strong></span></li>
      <li><span class="rc-yr">2022</span><span><strong>Gamedev.tv - Get GIT Smart Course</strong></span></li>
      <li><span class="rc-yr">2021</span><span><strong>Audiokinetic - Wwise 101</strong></span></li>
      <li><span class="rc-yr">2021</span><span><strong>Gamedev.tv - Unreal Engine Blueprint Game Developer</strong></span></li>
      <li><span class="rc-yr">2016</span><span><strong>Berklee College of Music, Coursera - Developing Your Musicianship</strong></span></li>
      <li><span class="rc-yr">2014</span><span><strong>ETS - TOEFL ITP</strong></span></li>
      <li><span class="rc-yr">2009</span><span><strong>Dancefloor DJ Academy - Music Production - Dancemusic Master</strong></span></li>
      <li><span class="rc-yr">2009</span><span><strong>Dancefloor DJ Academy - DJ - Dancemusic Master</strong></span></li>
    </ul>
  </div>

  <!-- EDUCATION -->
  <div class="rc-section" id="rc-education">
    <p class="rc-eyebrow">BACKGROUND</p>
    <h2 style="font-size:22px;">Education</h2>
    <ul class="rc-simple-list">
      <li><span class="rc-yr">2020</span><span><strong>Wwise Course</strong> — School of Video Game Audio</span></li>
      <li><span class="rc-yr">2015</span><span><strong>Arts Bachelor (Level 6)</strong> — Federal University of Bahia (UFBA), Brazil</span></li>
    </ul>
  </div>

  <!-- SOCIAL -->
  <div class="rc-section" id="rc-contact">
    <p class="rc-eyebrow">GET IN TOUCH</p>
    <div class="rc-social-row">
      <a class="rc-social-link" href="https://www.linkedin.com/in/nicvieira-audio/" target="_blank" rel="noopener" aria-label="LinkedIn">in</a>
      <a class="rc-social-link" href="https://github.com/nico-audio" target="_blank" rel="noopener" aria-label="GitHub"><i class="fab fa-github"></i></a>
    </div>
  </div>

</div>

<script>
  var rcSlideIndex = 1;
  rcShowSlides(rcSlideIndex);

  function rcShowSlides(n){
    var slides = document.querySelectorAll('#rcCarouselMain .rc-carousel-slide');
    var thumbs = document.querySelectorAll('#rcCarouselThumbs .rc-carousel-thumb');
    if (n > slides.length) rcSlideIndex = 1;
    if (n < 1) rcSlideIndex = slides.length;
    slides.forEach(function(s){ s.classList.remove('is-active'); });
    thumbs.forEach(function(t){ t.classList.remove('is-active'); });
    slides[rcSlideIndex - 1].classList.add('is-active');
    thumbs[rcSlideIndex - 1].classList.add('is-active');
  }
  function rcCurrentSlide(n){ rcShowSlides(rcSlideIndex = n); }
  function rcPlusSlides(n){ rcShowSlides(rcSlideIndex += n); }

  setInterval(function(){ rcPlusSlides(1); }, 5000);
</script>