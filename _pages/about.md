---
permalink: /
custom_class: about-page
title:
author_profile: false
redirect_from: 
  - /about/
  - /about.html
---
<div class="hero-container">
  <div class="hero-images">
    <img id="hero-img-1" src="" alt="image_1">
    <img id="hero-img-2" src="" alt="image_2">
    <img id="hero-img-3" src="" alt="image_3">
  </div>
  <div class="hero-text">
    <h1>WELCOME</h1>
    <p>Welcome to my personal page</p>
  </div>
</div>

<script>
  document.addEventListener("DOMContentLoaded", function () {
    const totalImages = 20;

    const usedIndexes = new Set();
    const getUniqueImage = () => {
      let num;
      do {
        num = Math.floor(Math.random() * totalImages) + 1;
      } while (usedIndexes.has(num));
      usedIndexes.add(num);
      return `/images/gallery/image_${num}.jpg`;
    };

    document.getElementById("hero-img-1").src = getUniqueImage();
    document.getElementById("hero-img-2").src = getUniqueImage();
    document.getElementById("hero-img-3").src = getUniqueImage();
  });
</script>
