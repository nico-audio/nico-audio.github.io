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
    <iframe width="560" height="315" src="https://www.youtube.com/embed/zy9apla4ko4?si=JM6dMMV3uD0z6Yx3" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>
  </div>
</div>

_This showreel contains some of my work such as the magic sound effects in **Grid Force - Mask of the Goddess (Dreamnauts studios)** and the splash screen for **SGC - Short Games Collection #1 (Nerd Monkeys)**  and redesigns where I re-create an entire scene from scratch._


# TECHNICAL VIDEOS 
<div class="video-gallery">
  <div class="grid-container">
    <div class="grid">
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/hTh3U1SofZo?si=ekdQWQ3-aKCitOq7er " frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> <b>UE5</b> - Dynamic footstep system implementation using Metasounds</div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/uZTqMzPiV8M?si=Yn2pUWRg1ahXKD-f" frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> Soundscaping in <b>Unity</b> using coroutines</div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/wJS7oHe3OCw?si=IgpRS6D4E3PRAYmx" frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> <b>Wwise</b> - Dynamic system based on day/night cycle to control the ambient sound </div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/cUD6vHqMwLU" frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> Demonstrating an implementation of the Doppler effect with custom parameters defined by a <b>C# script in Unity</b> <a href="https://nico-audio.github.io/posts/doppler-effect/" frameborder="0" allowfullscreen>(Tutorial here)</a> </div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/X8SD_jf_PII" frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> An implementation of the Doppler effect with <b>Pure data</b> <a href="https://nico-audio.github.io/posts/doppler-effect/">(Tutorial here)</a></div>
      </div>
      <div class="grid-item">
        <iframe src="https://www.youtube.com/embed/Gj6VqbLJr6I" frameborder="0" allowfullscreen></iframe>
        <div class="video-text"> A sound design tool created with <b>Pure Data</b> <a href="https://nico-audio.github.io/posts/easteregg/">(Tutorial here)</a></div>
      </div>
    </div>
  </div>
</div>


# MORE SOUND DESIGN

  <div class="video-gallery">
    <div class="grid-container">
      <div class="grid">
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/69eluR8comA?si=tNQjGMXMFmcJ8hwZ" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Splash Screen</b> sound design for Short Games Collection #1 (Nerd Monkeys) </div>
        </div>
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/XceLiKuplqI?si=4Lw5cmJkMbfrMjbC" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Magic spells</b> sound design for Grid Force - Mask of the Goddess </div>
        </div>
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/Tf7n4G2A3Tg?si=hKdmI-qt4s71avpu" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Magic spells</b> sound redesign for It takes two by Hazelight Studios</div>
        </div>
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/_5OLb5FeOJE?si=aXbYVjx_tn4-sL-F" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Monster attacks</b> sound redesign made for MTS (Airwiggles sound design challenge). Elements is 3rd-person open-world adventure RPG about two siblings fulfilling their destiny. <a href="https://store.steampowered.com/app/1468110/Elements/" target="_blank">(Steam)</a></div>
        </div>
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/ShWSV1enQIc?si=Zg5zMi88NokrHmUS" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Machinery</b> sound redesign made for MTS (Airwiggles sound design challenge).</div>
        </div>
        <div class="grid-item">
          <iframe src="https://www.youtube.com/embed/ccJ3gb8eM8s?si=XXaGemddxMUIf_Lh" frameborder="0" allowfullscreen></iframe>
          <div class="video-text"> <b>Mining game</b> sound redesign made for MTS (Airwiggles sound design challenge). Dig Dig Boom is a strategic mining adventure by SteinMakesGames where puzzles meet explosives. <a href="https://store.steampowered.com/app/2026040/Dig_Dig_Boom/" target="_blank">(Steam)</a> </div>
        </div>          