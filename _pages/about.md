---
title: "About"
date: 2025-05-03
layout: page
permalink: /
authors: []
---

<div class="hero-wrapper">
  <div class="hero-overlay">
    <h1>WELCOME</h1>
    <p>Welcome to my personal page</p>
  </div>
  <div class="hero-images-row">
    <img id="hero-img-1" src="" alt="image_1">
    <img id="hero-img-2" src="" alt="image_2">
    <img id="hero-img-3" src="" alt="image_3">
  </div>
</div>

<style>
.hero-wrapper {
  position: relative;
  width: 100%;
  height: 60vh;
  overflow: hidden;
}

.hero-images-row {
  display: flex;
  width: 100%;
  height: 100%;
}

.hero-images-row img {
  flex: 1;
  width: 100%;
  height: 100%;
  object-fit: cover;
}

.hero-overlay {
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
  color: white;
  text-align: center;
  text-shadow: 2px 2px 8px rgba(0,0,0,0.7);
  z-index: 2;
}

.hero-overlay h1 {
  font-size: 4em;
  margin: 0;
}

.hero-overlay p {
  font-size: 2em;
}
</style>

<script>
document.addEventListener("DOMContentLoaded", function () {
  const totalImages = 20;
  const usedIndexes = new Set();

  function getUniqueImage() {
    let num;
    do {
      num = Math.floor(Math.random() * totalImages) + 1;
    } while (usedIndexes.has(num));
    usedIndexes.add(num);
    return `/images/gallery/image_${num}.jpg`;
  }

  document.getElementById("hero-img-1").src = getUniqueImage();
  document.getElementById("hero-img-2").src = getUniqueImage();
  document.getElementById("hero-img-3").src = getUniqueImage();
});
</script>

