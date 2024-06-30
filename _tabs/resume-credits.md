---
title: RESUME / CREDITS
icon: fas fa-info-circle
order: 4
---

<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <!-- Open Graph meta tags -->
    <meta property="og:title" content="Resume / Credits" />
    <meta property="og:description" content="Nico's portfolio" />
    <meta property="og:image" content="https://raw.githubusercontent.com/nico-audio/nico-audio.github.io/main/assets/img/logo_alpha_nico.png" />
    <meta property="og:url" content="https://nico-audio.github.io/resume-credits/" />
    <title>Resume / Credits</title>
    <style>
        body {
            text-align: left; /* Center-aligns the title */
            background-color: #1b1b1e;
            color: #cccccc;
            margin: 0;
            padding: 0;
        }
        h1 {
           text-align: center; /* Center-align all h1 headings */
        }
        /* Styling for the carousel container */
        .carousel-container {
            position: relative;
            max-width: 800px;
            margin: auto;
            margin-top: 50px;
        }
        .carousel-main {
            position: relative;
            overflow: hidden;
            max-height: 400px;
        }
        .carousel-main img {
            width: 100%;
            height: auto;
            display: none;
        }
        .carousel-main img.active {
            display: block;
        }
        /* Styling for the image previews */
        .carousel-previews {
            display: flex;
            justify-content: center;
            gap: 10px;
            margin-top: 10px;
        }
        .carousel-previews img {
            width: auto;
            height: 50px;
            cursor: pointer;
            opacity: 0.6;
            transition: opacity 0.3s;
            object-fit: cover;
        }
        .carousel-previews img:hover,
        .carousel-previews img.active {
            opacity: 1;
        }
        /* Styling for the previous and next buttons */
        .prev, .next {
            cursor: pointer;
            position: absolute;
            top: 50%;
            width: auto;
            padding: 16px;
            margin-top: -22px;
            color: white;
            font-weight: bold;
            font-size: 18px;
            transition: 0.3s;
            user-select: none;
        }
        .prev {
            left: 0;
        }
        .next {
            right: 0;
        }
        .prev:hover, .next:hover {
            background-color: rgba(0, 0, 0, 0.8);
        }
        .linkedin-section {
            text-align: center;
            margin-top: 20px;
        }
    </style>
<!-- CREDITS -->
</head>
<body>
    <div class="carousel-container">
        <div class="carousel-main">
             <!-- Images for the carousel with corresponding captions -->
            <a href="https://www.youtube.com/watch?v=FalEcRLGzhY" target="_blank">
            <img src="https://user-images.githubusercontent.com/110834120/249539750-8d4530ae-d3bf-4412-982b-44efe86eed53.png" alt="Image 1" class="carousel-slide active">
            </a>
            <a href="https://www.youtube.com/watch?v=qfJY5a9Vzz8" target="_blank">
            <img src="https://github.com/nico-audio/nico-audio.github.io/assets/110834120/68df4e8d-e827-4688-9bca-12cadc3d7e85" alt="Image 2" class="carousel-slide">
            </a>
            <img src="https://github.com/nico-audio/nico-audio.github.io/assets/110834120/a076e0c1-7e89-40b3-a5ba-f23488cffae4" alt="Image 3" class="carousel-slide">
            <a class="prev" onclick="plusSlides(-1)">&#10094;</a>
            <a class="next" onclick="plusSlides(1)">&#10095;</a>
        </div>
        <div class="carousel-previews">
            <img src="https://user-images.githubusercontent.com/110834120/249539750-8d4530ae-d3bf-4412-982b-44efe86eed53.png" alt="Image 1" class="preview active" onclick="currentSlide(1)">
            <img src="https://github.com/nico-audio/nico-audio.github.io/assets/110834120/68df4e8d-e827-4688-9bca-12cadc3d7e85" alt="Image 2" class="preview" onclick="currentSlide(2)">
            <img src="https://github.com/nico-audio/nico-audio.github.io/assets/110834120/a076e0c1-7e89-40b3-a5ba-f23488cffae4" alt="Image 3" class="preview" onclick="currentSlide(3)">
        </div>
    </div>
    <!-- JS -->
    <script>
        let slideIndex = 1;
        showSlides(slideIndex);
        function showSlides(n) {
            let i;
            let slides = document.getElementsByClassName("carousel-slide");
            let previews = document.getElementsByClassName("preview");
            if (n > slides.length) {
                slideIndex = 1;
            }
            if (n < 1) {
                slideIndex = slides.length;
            }
            for (i = 0; i < slides.length; i++) {
                slides[i].style.display = "none";
            }
            for (i = 0; i < previews.length; i++) {
                previews[i].className = previews[i].className.replace(" active", "");
            }
            slides[slideIndex - 1].style.display = "block";
            previews[slideIndex - 1].className += " active";
        }
        function currentSlide(n) {
            showSlides(slideIndex = n);
        }
        function plusSlides(n) {
            showSlides(slideIndex += n);
        }
        setInterval(() => {
            plusSlides(1);
        }, 5000); // Change image every 5 seconds
    </script>    
</body>
</html>
<!-- CREDITS END -->
<!-- RESUME -->
<h2 style="text-align: left;">RELEASED TITLES</h2>

------------

- 2021 - <a href="https://store.steampowered.com/app/1379960/Grid_Force__Mask_Of_The_Goddess/" target="_blank"> Grid Force - Mask of the Goddess (Dreamnauts studios)</a> 
     - **Sound designer** - I designed elemental magic for characters in this game and composed a leitmotif.
- 2021 - <a href="https://www.nintendo.com/store/products/sgc-short-games-collection-1-switch/" target="_blank"> SGC - Short Games Collection #1 (Nerd Monkeys)</a>  
    - **Sound designer**, I designed the splash screen that opens the collection
- 2020 - <a href="https://www.legendsoflearning.com/math-basecamp/" target="_blank"> Fracture (StaalMedia, Nerd Monkeys)</a>  
    - **Audio designer**, I was part of the development team, designing sounds and helping in audio development in this educational math game.

<h2 style="text-align: left;">LANGUAGE SKILLS</h2>

------------

- **Portuguese** (Native)
- **English** (Proficient)
- **Spanish** (Intermediate)
- **Catalan** (Intermediate)

<h2 style="text-align: left;">PROGRAMMING / SOFTWARE SKILLS</h2>

------------
Wwise, Unreal Engine, Unity Engine, Reaper, Ableton Live, Pure Data, C#, Unreal Blueprints

<h2 style="text-align: left;">CERTIFICATIONS AND TRAINING</h2>

------------
- 2023 - **Audiokinetic - Wwise 251 - Performance Optimization & Mobile Considerations**
- 2022 - **Audiokinetic - Wwise 201 - Interactive Music**
- 2022 - **Gamedev.tv - Complete C# Unity Game Developer 2D Online Course**
- 2022 - **Gamedev.tv - Get GIT Smart Course**
- 2021 - **Audiokinetic - Wwise 101**
- 2021 - **Gamedev.tv - Unreal Engine Blueprint Game Developer**
- 2016 - **Berklee College of Music, Coursera - Developing Your Musicianship**
- 2014 - **ETS - TOEFL ITP**
- 2009 - **Dancefloor DJ Academy - Music Production - Dancemusic Master**
- 2009 - **Dancefloor DJ Academy - DJ - Dancemusic Master**

<h2 style="text-align: left;">EDUCATION</h2>

------------

- 2020 - **Wwise Course** - School of Video Game Audio
- 2015 - **Arts Bachelor (Level 6)** - Federal University of Bahia (UFBA), Salvador, Brazil

------------

<a href="https://www.linkedin.com/in/nicvieira-audio/" target="_blank" rel="noopener noreferrer" class="linkedin-link">
  <img src="https://user-images.githubusercontent.com/110834120/249790058-0574e658-33ae-4467-9e4f-50d5a092d36f.png" alt="LinkedIn Icon" width="30" height="30">
  <span>Connect with me on LinkedIn</span>
</a>