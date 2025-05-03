---
title: "About"
date: 2025-05-03
layout: page
permalink: /
authors: []
---

<div class="custom-hero-container">
  <div class="custom-hero-images">
    <img id="hero-img-1" src="" alt="Random image 1">
    <img id="hero-img-2" src="" alt="Random image 2">
    <img id="hero-img-3" src="" alt="Random image 3">
  </div>
  <div class="custom-hero-text">
    <h1>WELCOME</h1>
    <p>Welcome to my personal page.</p>
  </div>
</div>

<style>
.custom-hero-container {
  display: flex;
  flex-wrap: wrap;
  align-items: center;
  justify-content: center;
  margin-top: 2rem;
}

.custom-hero-images {
  display: flex;
  gap: 10px;
  flex: 1;
  justify-content: center;
  flex-wrap: wrap;
}

.custom-hero-images img {
  width: 200px;
  height: auto;
  object-fit: cover;
  border-radius: 6px;
  box-shadow: 0 2px 6px rgba(0, 0, 0, 0.1);
}

.custom-hero-text {
  flex: 1;
  text-align: center;
  margin-top: 20px;
}

@media (min-width: 768px) {
  .custom-hero-container {
    flex-wrap: nowrap;
  }
  .custom-hero-text {
    margin-top: 0;
    padding-left: 2rem;
    text-align: left;
  }
}
</style>

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
    return "/images/gallery/image_" + num + ".jpg";
  };

  document.getElementById("hero-img-1").src = getUniqueImage();
  document.getElementById("hero-img-2").src = getUniqueImage();
  document.getElementById("hero-img-3").src = getUniqueImage();
});
</script>
