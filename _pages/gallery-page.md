---
title: " "
layout: gallery
permalink: /gallery-page/
header:
  overlay_image: /assets/images/Gallery_IMG.png

# GAME ART
gallery_game:
  - image_path: /assets/images/WolfScopeArt.png
    alt: "Dr Scope character concept art"
    caption: "Final concept art of antagonist Dr Scope for Feral"

  - image_path: /assets/images/AxlArt.png
    alt: "AXL protagonist character concept art"
    caption: "Final concept art of protagonist AXL for Feral"

  - image_path: /assets/images/RatArtGame.png
    alt: "Rat character and environment concept art"
    caption: "Concept art exploring protagonist and environment design for Flicker"

  - image_path: /assets/images/BirdScopeArt.png
    alt: "Early Dr Scope concept art sketch"
    caption: "Early concept exploration for antagonist Dr Scope in Feral"

  - image_path: /assets/images/ClownArt.png
    alt: "Clown character card artwork"
    caption: "Character card design for The Clown in The Eternal Circus"

  - image_path: /assets/images/BaloondogArt.png
    alt: "Balloon dog prop card artwork"
    caption: "Prop card design: Balloon Dog for The Eternal Circus"

  - image_path: /assets/images/PickPocketArt.png
    alt: "Pickpocket action card artwork"
    caption: "Action card design: Pickpocket for The Eternal Circus"

  - image_path: /assets/images/FirebreatherArt.png
    alt: "Firebreather character card artwork"
    caption: "Character card design for The Firebreather in The Eternal Circus"

  - image_path: /assets/images/AnimalContainment.png
    alt: "Feral containment zone environment art"
    caption: "Environment concept showing hybrid containment zone in Feral"

  - image_path: /assets/images/LeoFrogDesign.png
    alt: "Hybrid frog NPC character design"
    caption: "Character design for an intelligent hybrid NPC in Feral"

  - image_path: /assets/images/ScopeDesign.png
    alt: "Dr Scope character design"
    caption: "Character design exploration for Dr Scope in Feral"

  - image_path: /assets/images/ScopesOfficeResized.png
    alt: "Dr Scope office environment art"
    caption: "Environment design for Dr Scope’s office in Feral"


# GENERAL ART
gallery_general:
  - image_path: /assets/images/DaisukeArt.png
    alt: "Daisuke fan art from Mouthwashing"
    caption: "Fan art of Daisuke from video game Mouthwashing"

  - image_path: /assets/images/CatArt.png
    alt: "Cat expression study sketch"
    caption: "Expression study exploring character emotion through a cat"

  - image_path: /assets/images/NeytiriArt.png
    alt: "Neytiri fan art from Avatar"
    caption: "Fan art of Neytiri from movie Avatar"

  - image_path: /assets/images/PhenomamanArt.png
    alt: "Phenomaman fan art character"
    caption: "Fan art of Phenomaman from game Dispatch created for a contest"

  - image_path: /assets/images/HumanStudyArt.png
    alt: "Humanoid angel character study"
    caption: "Original character study exploring a humanoid angel design"

  - image_path: /assets/images/SnowLeopardArt.png
    alt: "Anthropomorphic snow leopard character"
    caption: "Original character design: anthropomorphic snow leopard"

  - image_path: /assets/images/WolfArt.png
    alt: "Anthropomorphic wolf character"
    caption: "Original character design: anthropomorphic wolf"

  - image_path: /assets/images/RavenArt.png
    alt: "Anthropomorphic raven character"
    caption: "Another individuals character design I reimagined for Art Fight"
---

<style>
/* GRID */
.gallery-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(220px, 1fr));
  gap: 1.5rem;
}

.gallery-card {
  background: #f3f3f3;
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

.custom-footer,
#main,
.page,
.page__content {
  position: relative;
  z-index: 1;
}

.lightbox {
  position: fixed;
  inset: 0;
  background: rgba(0,0,0,0.95);
  display: none;
  justify-content: center;
  align-items: center;
  z-index: 9999999999;
}

.lightbox.active {
  display: flex;
}

.lightbox img {
  max-width: 90%;
  max-height: 90%;
}

/* ARROWS */
.lightbox-arrow {
  position: absolute;
  top: 50%;
  transform: translateY(-50%);
  font-size: 3rem;
  color: white;
  cursor: pointer;
  padding: 1rem;
  user-select: none;
}

.lightbox-arrow.left { left: 20px; }
.lightbox-arrow.right { right: 20px; }

/* LOCK SCROLL */
body.lightbox-open {
  overflow: hidden;
}
</style>

## About The Gallery
This is my collection of artwork including game-related pieces and general work

---

## Game Art
<div class="gallery-grid">
{% for item in page.gallery_game %}
  <div class="gallery-card" onclick="openLightbox({{ forloop.index0 }}, 'game')">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    <div class="gallery-text">{{ item.caption }}</div>
  </div>
{% endfor %}
</div>

---

## General Art
<div class="gallery-grid">
{% for item in page.gallery_general %}
  <div class="gallery-card" onclick="openLightbox({{ forloop.index0 }}, 'general')">
    <img src="{{ item.image_path }}" alt="{{ item.alt }}">
    <div class="gallery-text">{{ item.caption }}</div>
  </div>
{% endfor %}
</div>

<!-- LIGHTBOX -->
<div id="lightbox" class="lightbox" onclick="closeLightbox()">
  <span class="lightbox-arrow left" onclick="event.stopPropagation(); prevImage()">❮</span>
  <img id="lightbox-img" src="">
  <span class="lightbox-arrow right" onclick="event.stopPropagation(); nextImage()">❯</span>
</div>

<script>
let currentIndex = 0;
let currentGallery = [];

let gameGallery = [
{% for item in page.gallery_game %}
  "{{ item.image_path }}",
{% endfor %}
];

let generalGallery = [
{% for item in page.gallery_general %}
  "{{ item.image_path }}",
{% endfor %}
];

function openLightbox(index, type) {
  currentIndex = index;
  currentGallery = (type === 'game') ? gameGallery : generalGallery;

  document.getElementById("lightbox").classList.add("active");
  document.body.classList.add("lightbox-open");
  updateImage();
}

function closeLightbox() {
  document.getElementById("lightbox").classList.remove("active");
  document.body.classList.remove("lightbox-open");
}

function updateImage() {
  document.getElementById("lightbox-img").src = currentGallery[currentIndex];
}

function nextImage() {
  currentIndex = (currentIndex + 1) % currentGallery.length;
  updateImage();
}

function prevImage() {
  currentIndex = (currentIndex - 1 + currentGallery.length) % currentGallery.length;
  updateImage();
}

document.addEventListener("keydown", function(e) {
  if (!document.getElementById("lightbox").classList.contains("active")) return;

  if (e.key === "ArrowRight") nextImage();
  if (e.key === "ArrowLeft") prevImage();
  if (e.key === "Escape") closeLightbox();
});
</script>
