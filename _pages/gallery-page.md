---
title: " "
layout: gallery
permalink: /gallery-page/
header:
  overlay_image: /assets/images/Gallery_IMG.png

# GAME ART
gallery_game:
  - image_path: /assets/images/BirdScopeArt.png
    alt: "Game art 1"
    caption: "Test"
  - image_path: /assets/images/WolfScopeArt.png
    alt: "Game art 2"
    caption: "Test"
  - image_path: /assets/images/MonkeyScopeArt.png
    alt: "Game art 3"
    caption: "Test"
  - image_path: /assets/images/BunnySketch.png
    alt: "Game art 4"
    caption: "Test"
  - image_path: /assets/images/AxlArt.png
    alt: "Game art 5"
    caption: "Test"
  - image_path: /assets/images/RatArtGame.png
    alt: "Game art 6"
    caption: "Test"
  - image_path: /assets/images/ClownArt.png
    alt: "Game art 7"
    caption: "Test"
  - image_path: /assets/images/BaloondogArt.png
    alt: "Game art 8"
    caption: "Test"
  - image_path: /assets/images/FirebreatherArt.png
    alt: "Game art 9"
    caption: "Test"
  - image_path: /assets/images/CageArt.png
    alt: "Game art 10"
    caption: "Test"
  - image_path: /assets/images/PickPocketArt.png
    alt: "Game art 11"
    caption: "Test"
  - image_path: /assets/images/CircusArt.png
    alt: "Game art 12"
    caption: "Test"

# GENERAL ART
gallery_general:
  - image_path: /assets/images/DaisukeArt.png
    alt: "General art 1"
    caption: "Test"
  - image_path: /assets/images/CatArt.png
    alt: "General art 2"
    caption: "Test"
  - image_path: /assets/images/NeytiriArt.png
    alt: "General art 3"
    caption: "Test"
---

<style>
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.gallery-card {
  background: linear-gradient(to bottom, #ffffff, #e9dcbe);
  border-radius: 12px;
  overflow: hidden;
  cursor: pointer;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.gallery-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 25px rgba(0,0,0,0.15);
}

.gallery-card img {
  width: 100%;
  height: auto;
  display: block;
}

.gallery-text {
  padding: 0.75rem;
  font-size: 0.9rem;
  text-align: center;
}

.lightbox {
  position: fixed;
  top: 0;
  left: 0;
  width: 100%;
  height: 100%;
  background: rgba(0,0,0,0.9);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 9999;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
}

.lightbox.active {
  display: flex;
}
</style>

## About The Gallery
This is my collection of artwork including game-related pieces and general work

---

## Game Art
<div id="game-art"></div>

<div class="gallery-grid">
{% for item in page.gallery_game %}
  <div class="gallery-card" onclick="openLightbox('{{ item.image_path }}')">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    {% if item.caption %}
      <div class="gallery-text">{{ item.caption }}</div>
    {% endif %}
  </div>
{% endfor %}
</div>

---

## General Art
<div id="general-art"></div>

<div class="gallery-grid">
{% for item in page.gallery_general %}
  <div class="gallery-card" onclick="openLightbox('{{ item.image_path }}')">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    {% if item.caption %}
      <div class="gallery-text">{{ item.caption }}</div>
    {% endif %}
  </div>
{% endfor %}
</div>

<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <img id="lightbox-img" src="">
</div>

<script>
function openLightbox(src) {
  document.getElementById("lightbox").classList.add("active");
  document.getElementById("lightbox-img").src = src;
}

function closeLightbox() {
  document.getElementById("lightbox").classList.remove("active");
}
</script>
