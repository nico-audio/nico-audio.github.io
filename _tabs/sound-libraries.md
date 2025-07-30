---
#layout: categories
title: SOUND LIBRARIES
icon: fas fa-stream
order: 5
---

<style>

/* Logo */
.logo {
    max-width: 100%;
    max-height: 100%;
    height: auto;
    width: 200px;
}

.logo-container {
    text-align: center;
}

/* Gallery view */
.image-gallery{
  margin: 20px 0;
  /*overflow: hidden; 
  padding: 10px 0;*/
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
  text-align: center;
  background-color: rgb(45, 46, 50); /* Charcoal gray */
  border-radius: 15px;
  padding: 1.5rem;
  transition: transform 0.3s ease-in-out, border-color 0.3s ease-in-out;
  border: 1px solid #444;
}

.grid-item:hover {
  transform: scale(1.02);
  border-color: #888;
  z-index: 10;
}

.grid-item iframe {
  width: 350px;
  height: 225px;
  object-fit: cover;
  border: 0px;
}

/* Product Text */
.product-text {
  margin: 1.25rem 0;
  color: #ccc;
}

.product-text h4 {
  margin: 0 0 0.5rem 0;
  color: #fff;
  font-size: 1.2rem;
}

.product-text p {
  margin: 0;
  font-size: 0.9rem;
  /*text-align: justify;*/
}

/* Buttons */
.purchase-button {
  text-align: center;
  margin-top: 1rem;
}

.learn-more-button {
    display: block;
    width: -moz-fit-content;
    width: fit-content;
    margin: 0.5rem auto 0;
    padding: 8px 16px;
    font-size: 14px;
    text-decoration: none;
    border: none;
    outline: none;
    color: #fff;
    background: #111;
    cursor: pointer;
    position: relative;
    z-index: 0;
    border-radius: 10px;
}

.learn-more-button:before {
    content: '';
    background: linear-gradient(45deg, #ff0000, #ff7300, #fffb00, #48ff00, #00ffd5, #002bff, #7a00ff, #ff00c8, #ff0000);
    position: absolute;
    top: -2px;
    left:-2px;
    background-size: 400%;
    z-index: -1;
    filter: blur(5px);
    width: calc(100% + 4px);
    height: calc(100% + 4px);
    animation: glowing 20s linear infinite;
    opacity: 0;
    transition: opacity .3s ease-in-out;
    border-radius: 10px;
}

.learn-more-button:hover:before {
    opacity: 1;
}

.learn-more-button:after {
    z-index: -1;
    content: '';
    position: absolute;
    width: 100%;
    height: 100%;
    background: #111;
    left: 0;
    top: 0;
    border-radius: 10px;
}

.learn-more-button:active {
    color: #000
}

.learn-more-button:active:after {
    background: transparent;
}

/* Mobile responsiveness */
@media (max-width: 768px) {
  .grid {
    grid-template-columns: repeat(1, 1fr);
  }

  .grid-item {
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

@keyframes glowing {
    0% { background-position: 0 0; }
    50% { background-position: 400% 0; }
    100% { background-position: 0 0; }
}
</style>

<!-- Gumroad button -->
<script src="https://gumroad.com/js/gumroad.js"></script>

<!-- Logo -->
<div class="logo-container">
  <img src="/assets/img/Spectrum-logo.png" alt="Spectrum Logo" class="logo">
</div>

<!-- Intro text -->
<p>In the last years I've dedicated a lot of time into collecting, exploring and working on sounds. Now I want to share some of it, that's why I've created <a href="https://spectrumlibraries.com" target="_blank" rel="noopener noreferrer"> Spectrum Libraries.</a></p>
<br />

<!-- Gallery view -->
<div class="image-gallery">
  <div class="grid-container">
    <div class="grid">
      <div class="grid-item">
        <img src="/assets/img/Skateboard_thumbnail.png" alt="Skateboard Sound Library" style="max-width: 100%; height: auto; border-radius: 8px;" width="300" height="300"/>
        <div class="product-text">
          <h4>SKATEBOARD</h4>
          <p>96kHz, 24 bit, 100% royalty-free sound library recorded across different skateparks. Includes UCS compliant metadata.</p>
        </div>
        <div class="purchase-button">
          <a class="gumroad-button" href="https://spectrumlibraries.gumroad.com/l/skateboard">Buy on</a>
          <a href="https://spectrumlibraries.com/skateboard" target="_blank" class="learn-more-button">Learn More</a>
        </div>
      </div>
      <div class="grid-item">
        <img src="/assets/img/Interfaces_thumbnail.png" alt="Interfaces Sound Library" style="max-width: 100%; height: auto; border-radius: 8px;" width="300" height="300"/>
        <div class="product-text">
          <h4>INTERFACES</h4>
          <p>96kHz, 24 bit, 100% royalty-free sound library featuring designed user interface sounds. Includes UCS compliant metadata.</p>
        </div>
        <div class="purchase-button">
          <a class="gumroad-button" href="https://spectrumlibraries.gumroad.com/l/interfaces">Buy on</a>
          <a href="https://spectrumlibraries.com/interfaces" target="_blank" class="learn-more-button">Learn More</a>
        </div>
      </div>
    </div>
  </div>
</div>
