---
title: PROGRAMMING
icon: fas fa-stream
order: 3
---

<style>
  .card {
    /* Add a transition for a smooth effect */
    transition: box-shadow 0.2s ease-in-out;
  }
  .card:hover {
    /* Add a simple highlight around the box */
    box-shadow: 0 0 0 2px rgba(255, 255, 255, 0.4);
  }
  .card-footer {
    background-color: #38383b;
  }
</style>

Here are some of the projects and tools I've worked on. Some of them are part of the tutorials on this website.

## Audio programming

<div class="row">
  <div class="col-lg-6 mb-4">
    <div class="card h-100" style="background-color: #313134;">
      <a href="/posts/easteregg/">
        <img class="card-img-top" src="_posts/img/EasterEgg/Fig1_EasterEgg_patch.png" alt="Easter Egg Sound Design Tool">
      </a>
      <div class="card-body">
        <h4 class="card-title">
          <a href="/posts/easteregg/">"Easter Egg" Sound Design Tool</a>
        </h4>
        <p class="card-text">A "happy accidents" sound design tool built in Pure Data. It allows for loading a sample, manipulating it through an FX chain, and capturing the output using a buffer.</p>
      </div>
      <div class="card-footer d-flex justify-content-between align-items-center">
        <div>
          <span class="badge badge-secondary">Pure Data</span>
          <span class="badge badge-secondary">Sound Design</span>
          <span class="badge badge-secondary">Tooling</span>
        </div>
        <a href="https://github.com/nico-audio/pd-patches/tree/master/easter-egg" target="_blank" rel="noopener" aria-label="github" class="text-muted">
          <i class="fab fa-github fa-lg"></i>
        </a>
      </div>
    </div>
  </div>

  <div class="col-lg-6 mb-4">
    <div class="card h-100" style="background-color: #313134;">
      <a href="/posts/doppler-effect/">
        <img class="card-img-top" src="_posts/img/DopplerEffect/doppler-unity.gif" alt="The Doppler Effect in Unity">
      </a>
      <div class="card-body">
        <h4 class="card-title">
          <a href="/posts/doppler-effect/">The Doppler Effect in Unity and Pure data</a>
        </h4>
        <p class="card-text">A custom implementation of the Doppler effect in Unity, with a C# script to control the pitch shift of a moving audio source relative to a listener. This project demonstrates how to apply audio physics for more immersive game environments.</p>
      </div>
      <div class="card-footer d-flex justify-content-between align-items-center">
        <div>
          <span class="badge badge-secondary">Unity</span>
          <span class="badge badge-secondary">C#</span>
          <span class="badge badge-secondary">Game Audio</span>
          <span class="badge badge-secondary">Pure Data</span>
        </div>
        <a href="https://github.com/nico-audio/pd-patches" target="_blank" rel="noopener" aria-label="github" class="text-muted">
          <i class="fab fa-github fa-lg"></i>
        </a>
      </div>
    </div>
  </div>

</div>

<hr>

## Game Development

<div class="row">
  <div class="col-lg-6 mb-4">
    <div class="card h-100" style="background-color: #313134;">
      <a href="https://github.com/nico-audio/GordonsIsland" target="_blank" rel="noopener">
        <img class="card-img-top" src="assets/img/gordon-v1.gif" alt="Gordon's Island">
      </a>
      <div class="card-body">
        <h4 class="card-title">
          <a href="https://github.com/nico-audio/GordonsIsland" target="_blank" rel="noopener">Gordon's Island</a>
        </h4>
        <p class="card-text">A 2D top-down adventure game made with C++ and Raylib.</p>
      </div>
      <div class="card-footer d-flex justify-content-between align-items-center">
        <div>
          <span class="badge badge-secondary">C++</span>
          <span class="badge badge-secondary">Raylib</span>
          <span class="badge badge-secondary">Game dev</span>
        </div>
        <a href="https://github.com/nico-audio/GordonsIsland" target="_blank" rel="noopener" aria-label="github" class="text-muted">
          <i class="fab fa-github fa-lg"></i>
        </a>
      </div>
    </div>
  </div>
</div>