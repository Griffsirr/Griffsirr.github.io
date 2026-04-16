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

# GENERAL ART
gallery_general:
  - image_path: /assets/images/DaisukeArt.png
    alt: "General art 1"
  - image_path: /assets/images/CatArt.png
    alt: "General art 2"
  - image_path: /assets/images/NeytiriArt.png
    alt: "General art 3"

---

## Gallery
This is my collection of artwork including game-related pieces and general work

## Game Art
<div id="game-art"></div>
{% include gallery id="gallery_game" layout="third" %}

## General Art
<div id="general-art"></div>
{% include gallery id="gallery_general" layout="third" %}
