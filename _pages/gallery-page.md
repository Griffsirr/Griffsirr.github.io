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
  - image_path: /assets/images/WolfScopeArt.png
    alt: "Game art 2"
  - image_path: /assets/images/MonkeyScopeArt.png
    alt: "Game art 3"
  - image_path: /assets/images/BunnySketch.png
    alt: "Game art 4"
  - image_path: /assets/images/AxlArt.png
    alt: "Game art 5"
  - image_path: /assets/images/RatArtGame.png
    alt: "Game art 6"
  - image_path: /assets/images/ClownArt.png
    alt: "Game art 7"
  - image_path: /assets/images/BaloondogArt.png
    alt: "Game art 8"
  - image_path: /assets/images/FirebreatherArt.png
    alt: "Game art 9"
  - image_path: /assets/images/CageArt.png
    alt: "Game art 10"
  - image_path: /assets/images/PickPocketArt.png
    alt: "Game art 11"
  - image_path: /assets/images/CircusArt.png
    alt: "Game art 12"
  - image_path: /assets/images/Screenshot 2026-04-16 145522.png
    alt: "Game art 13"
  - image_path: /assets/images/Screenshot 2026-04-16 144156.png
    alt: "Game art 14"
  - image_path: /assets/images/Screenshot 2026-04-16 144314.png
    alt: "Game art 15"

# GENERAL ART
gallery_general:
  - image_path: /assets/images/DaisukeArt.png
    alt: "General art 1"
  - image_path: /assets/images/CatArt.png
    alt: "General art 2"
  - image_path: /assets/images/NeytiriArt.png
    alt: "General art 3"
  - image_path: /assets/images/PhenomamanArt.png
    alt: "General art 4"
  - image_path: /assets/images/HumanStudyArt.png
    alt: "General art 5"
  - image_path: /assets/images/CabaretArt.png
    alt: "General art 6"
  - image_path: /assets/images/SnowLeopardArt.png
    alt: "General art 7"
  - image_path: /assets/images/RavenArt.png
    alt: "General art 8"
  - image_path: /assets/images/WolfArt.png
    alt: "General art 9"
---

<style>
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.gallery-card {
  background: #fff;
  border-radius: 12px;
  overflow: hidden;
  transition: transform 0.25s ease, box-shadow 0.25s ease;
}

.gallery-card:hover {
  transform: translateY(-6px);
  box-shadow: 0 12px 25px rgba(0,0,0,0.15);
}

.gallery-card img {
  width: 100%;
  height: 200px;
  object-fit: cover;
}

.gallery-text {
  padding: 0.75rem;
  font-size: 0.9rem;
  text-align: center;
}
</style>

## About The Gallery
This is my collection of artwork including game-related pieces and general work

---

## Game Art
<div id="game-art"></div>

<div class="gallery-grid">
{% for item in page.gallery_game %}
  <div class="gallery-card">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    <div class="gallery-text">
      Lorem ipsum dolor sit amet
    </div>
  </div>
{% endfor %}
</div>

---

## General Art
<div id="general-art"></div>

<div class="gallery-grid">
{% for item in page.gallery_general %}
  <div class="gallery-card">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    <div class="gallery-text">
      Lorem ipsum dolor sit amet
    </div>
  </div>
{% endfor %}
</div>
