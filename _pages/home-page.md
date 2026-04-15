---
title: " "
layout: homepage
permalink: /home-page/
header:
  overlay_image: /assets/images/Untitled design.png

  excerpt: "  "

skills:
  - name: "Unity Development"
    icon: "fab fa-fw fa-unity"
    badges: ["C#", "Prototyping", "Gameplay"]
    text: "Developed 2D and 3D game prototypes in Unity, focusing on core mechanics and responsive gameplay."
    years: 2

  - name: "Game Design"
    icon: "fas fa-fw fa-gamepad"
    badges: ["Mechanics", "Levels", "UX"]
    text: "Designed gameplay systems, levels and player feedback with a focus on engaging experiences."
    level_label: "Intermediate"

  - name: "Game Art & Visual Design"
    icon: "fas fa-fw fa-palette"
    badges: ["UI", "Assets", "Style"]
    text: "Created UI, pixel art and basic 3D assets, focusing on clarity and visual consistency."
    level_label: "Beginner"

  - name: "Narrative & Worldbuilding"
    icon: "fas fa-fw fa-book"
    badges: ["Story", "Lore", "Characters"]
    text: "Developed worlds, characters and narratives with a focus on immersion and storytelling."
    level_label: "Intermediate"


feature_row:
  - image_path: /assets/images/a8c2c734827e565c4c0a4e99dd3cf184.jpg
    alt: "Game art and visual design"
    title: "Game Art"
    excerpt: "A collection of my game-focused artwork, including pixel art, UI design and visual assets created for both 2D and 3D projects."
    url: "/gallery-page/#game-art"
    btn_label: "Game Art Gallery"
    btn_class: "btn--primary"

  - image_path: /assets/images/a8c2c734827e565c4c0a4e99dd3cf184.jpg
    alt: "Game development projects"
    title: "Game Projects"
    excerpt: "Explore the games I’ve developed using Unity and C#, including solo projects and collaborative work focused on gameplay, storytelling and design."
    url: "/projects-page/"
    btn_label: "View Projects"
    btn_class: "btn--primary"

  - image_path: /assets/images/a8c2c734827e565c4c0a4e99dd3cf184.jpg
    alt: "General digital and traditional art"
    title: "General Art"
    excerpt: "A wider showcase of my creative work, including digital illustrations, character designs and visual experiments outside of game development."
    url: "/gallery-page/#general-art"
    btn_label: "General Art Gallery"
    btn_class: "btn--primary"
---
<style>
   .btn--primary {
    background-color: #a18b6d !important;
    border-color: #a18b6d !important;
  }

  .btn--primary:hover {
    background-color: #524739 !important; 
    border-color: #524739 !important;
  }
  
  .feature__item {
    transition: transform 0.2s ease, box-shadow 0.2s ease;
  }

  .feature__item {
    text-align: center;
  }
  
  .feature__item:hover {
    transform: translateY(-5px);
    box-shadow: 0 10px 20px rgba(0,0,0,0.1);
  }

  

  .feature__item .btn {
  display: inline-block;
  margin-top: 0.5rem;
}

  .skill-title {
    color: #a18b6d;
    border-bottom: 2px solid #a18b6d;
  }

  .skill-card {
    transition: transform 0.25s ease, box-shadow 0.25s ease;
    border-radius: 10px;
  }

  .skill-card:hover {
    transform: translateY(-6px);
    box-shadow: 0 12px 25px rgba(0,0,0,0.12);
  }

</style>

## Featured
{% include feature_row %}




