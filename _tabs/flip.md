---
layout: page
title: Credits
order: 5
---

<style>
/* Flip Card Container */
.flip-card-container {
  display: flex;
  justify-content: center;
  align-items: center;
  flex-wrap: wrap;
  gap: 20px; /* Adjust the value to control the gap between flip cards */
}

/* Flip Card */
.flip-card {
  background-color: transparent;
  perspective: 1000px;
  width: 480px;
  height: 270px;
  margin: 0; /* Reset margin */
}

/* Flip Card Inner */
.flip-card-inner {
  width: 100%;
  height: 100%;
  text-align: center;
  transition: transform 0.4s ease-in-out; /* Adjust the transition timing for smoother flipping */
  transform-style: preserve-3d;
  box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);
}

/* Flip Card Front */
.flip-card-front,
.flip-card-back {
  position: absolute;
  width: 100%;
  height: 100%;
  backface-visibility: hidden;
}

/* Flip Card Front Styling */
.flip-card-front {
  background-color: #1b1b1e;
  display: flex;
  justify-content: center;
  align-items: center;
}

/* Flip Card Back Styling */
.flip-card-back {
  background-color: #333;
  color: #fff;
  transform: rotateY(180deg);
  padding: 20px;
}

/* Flip Card Image */
.flip-card-image {
  max-width: 100%;
  max-height: 100%;
  object-fit: cover;
  object-position: center;
}

/* Flip Card Text */
.flip-card-text {
  font-size: 16px;
  line-height: 1.6;
}

/* Flip Card Hover */
.flip-card:hover .flip-card-inner {
  transform: rotateY(180deg);
}

</style>

<div class="flip-card-container">
  <div class="flip-card">
    <div class="flip-card-inner">
      <div class="flip-card-front">
        <!-- Image goes here -->
        <img src="https://user-images.githubusercontent.com/110834120/249539750-8d4530ae-d3bf-4412-982b-44efe86eed53.png" alt="GridForce" class="flip-card-image">
      </div>
      <div class="flip-card-back">
        <!-- Information text goes here -->
        <div class="flip-card-text">
          <h3>Sound designer</h3>
          <p> <i>Grid Force - Mask of the Goddess (Dreamnauts) is a real-time tactical bullet-hell RPG with grid-based combat and a deep story that adapts to your choices.</i> <a href="https://store.steampowered.com/app/1379960/Grid_Force__Mask_Of_The_Goddess/"> 
          <br>Steam</a></p>
        </div>
      </div>
    </div>
  </div>
  
<div class="flip-card-container">
  <div class="flip-card">
    <div class="flip-card-inner">
      <div class="flip-card-front">
        <!-- Image goes here -->
        <img src="https://user-images.githubusercontent.com/110834120/249542604-fa437fe9-f8c2-4bec-98cf-093005ef68e6.png" alt="SGC" class="flip-card-image">
      </div>
      <div class="flip-card-back">
        <!-- Information text goes here -->
        <div class="flip-card-text">
          <h3>Sound designer</h3>
          <p><i>SGC - Short Games Collection #1 (Nerd Monkeys) - A curated selection of unique short videogame experiences, wrapped in an immersive dynamic menu.</i> <a href="https://www.nintendo.com/store/products/sgc-short-games-collection-1-switch/"> 
          <br>Nintendo Store</a></p>
        </div>
      </div>
    </div>
  </div>

  <div class="flip-card-container">
  <div class="flip-card">
    <div class="flip-card-inner">
      <div class="flip-card-front">
        <!-- Image goes here -->
        <img src="https://user-images.githubusercontent.com/110834120/249549426-bc0659a1-401f-4313-8c34-2d8d36e77ba6.png" alt="Fracture" class="flip-card-image">
      </div>
      <div class="flip-card-back">
        <!-- Information text goes here -->
        <div class="flip-card-text">
          <h3>Audio designer</h3>
          <p> <i>Fracture (Staal Media) - Educational math game for the Legends of Learning platform</i> </p>
        </div>
      </div>
    </div>
  </div>

  <!-- Add more flip cards as needed -->
  
</div>

