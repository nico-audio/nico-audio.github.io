---
#layout: categories
title: Demo
icon: fas fa-stream
order: 1
---

<style>
/*main video*/
.video-container {
  text-align: center;
}

.video-container iframe {
  width: 560px;
  height: 315px;
}
/*mobile responsiveness*/
@media (max-width: 767px) {
  .video-container {
    width: 100%;
  }

  .video-container iframe {
    width: 100%;
    height: auto;
  }
}

/* Video gallery */
.video-gallery {
  margin: 20px 0;
  overflow: hidden;
}

.grid-container {
  display: flex;
  justify-content: center;
  margin: 0;
}

.grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-gap: 20px;
}

.grid-item {
  position: relative;
  padding-bottom: 0;
}

.grid-item iframe {
  width: 350px;
  height: 225px;
  object-fit: cover;
  border: 0px;
}

.video-text {
  font-size: 14px;
  text-align: justify;
  margin-top: 0px;
  width: 100%;
  max-width: 350px;
  margin-left: auto;
  margin-right: auto;
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(1, 1fr);
  }

  .grid-item {
    padding-bottom: 0;
    width: 90%;
    margin-left: auto;
    margin-right: auto;
  }

  .grid-item iframe {
    width: 100%;
    height: auto;
    padding-bottom: 0;
  }
}
</style>


## SOUND DESIGN DEMO

<div style="text-align: center;">
  <div class="video-container">
    <iframe width="560" height="315" src="https://www.youtube.com/embed/mjOHrn_9Cf4" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </div>
</div>

_This showreel contains some of my work such as the sound design for the splash screen in SGC - Short Games Collection #1 (Nerd Monkeys) and the magic sound effects in Grid Force - Mask of the Goddess (Playtra Games) together with redesigns for other titles  where I re-create an entire scene from scratch._


# TECHNICAL VIDEOS 
<div class="video-gallery">
  <div class="grid-container">
    <div class="grid">
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/2PX0yoSkC6Q?si=arRtRas4RZE1M4mP"></iframe>
        <div class="video-text"> Soundscaping in Unity using coroutines</div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/sBPl59akKL8?si=622Jl9wQW-QoCw8W"></iframe>
        <div class="video-text"> Wwise - Dynamic system based on day/night cycle to control the ambient sound </div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/cUD6vHqMwLU"></iframe>
        <div class="video-text"> Demonstrating an implementation of the Doppler effect with custom parameters defined by a C# script in Unity <a href="https://nico-audio.github.io/posts/doppler-effect/">(Tutorial here)</a> </div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/X8SD_jf_PII"></iframe>
        <div class="video-text"> An implementation of the Doppler effect with Pure data <a href="https://nico-audio.github.io/posts/doppler-effect/">(Tutorial here)</a></div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/Gj6VqbLJr6I"></iframe>
        <div class="video-text"> A sound design tool created with Pure Data <a href="https://nico-audio.github.io/posts/easteregg/">(Tutorial here)</a></div>
      </div>
    </div>
  </div>
</div>