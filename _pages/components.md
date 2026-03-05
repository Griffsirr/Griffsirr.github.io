---
title: "Components"
layout: default
permalink: /components/
gallery_gameplay:
  # Recommended: width "240px" to "320px" keeps a neat grid
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 1"
    title: "Core loop"
    caption: "Core loop"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 2"
    title: "Challenge"
    caption: "Challenge"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 3"
    title: "Power-ups"
    caption: "Power-ups"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 4"
    title: "Boss arena"
    caption: "Boss arena"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 5"
    title: "UI feedback"
    caption: "UI feedback"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Gameplay 6"
    title: "Final tweak"
    caption: "Final tweak"

gallery_gameart:
  # Recommended: width "240px" to "320px" keeps a neat grid
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Art 1"
    title: "Style pass"
    caption: "Style pass"
  - url: /assets/images/placeholder.png
    image_path: /assets/images/placeholder.png
    alt: "Art 2"
    title: "Final polish"
    caption: "Final polish"
skills:
  - name: "Unity"
    icon: "fab fa-fw fa-unity"
    badges: ["C#", "Game Dev"]
    text: "Built multiple prototypes and a published jam game."
    years: 2
  - name: "Game Design"
    icon: "fas fa-fw fa-gamepad"
    badges: ["Game Mechanics", "Levels", "UI"]
    text: "Designed mechanics, levels, and player feedback loops."
    level_label: "Beginner"
feature_row:
  - image_path: /assets/images/placeholder.png
    alt: "placeholder image 1"
    title: "Placeholder 1"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
  - image_path: /assets/images/placeholder.png
    alt: "placeholder image 2"
    title: "Placeholder 2"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
    url: "#test-link"
    btn_label: "Read More"
    btn_class: "btn--primary"
  - image_path: /assets/images/placeholder.png
    alt: "placeholder image 4"
    title: "Placeholder 3"
    excerpt: "This is some sample content that goes here with **Markdown** formatting."
---

This page is a workspace for demonstrating available components. 
Examples of the following below:
1. [Text](#text)
2. [Hyperlink](#hyperlink)
3. [Quote](#quote)
4. [Logo](#logo)
5. [Favicon](#favicon)
6. [Image](#image)
7. [Gallery](#gallery)
8. [Second Gallery](#second-gallery)
9. [Video](#video)
10. [Standard button](#standard-button)
11. [Call to Action (CTA) Button](#call-to-action-cta-button)
12. [Skills](#skills)
13. [Feature row](#feature-row)
14. [Contact Form](#contact-form)


## 1. Use markdown to format text {#text}
<a href="https://www.markdownguide.org/basic-syntax/" target="_blank" rel="noopener noreferrer">Markdown Guide</a>.

## 2. Hyperlink - <a href="https://www.example.com" target="_blank" rel="noopener noreferrer">Example Hyperlink</a>. Open `components.md` page and copy this example. {#hyperlink}

## 3. Quote - Think of ways to use this in your portfolio and I don't want to see this quote used in your final portfolios! {#quote}

{% include quote text="This was the most polished student game I have ever played in my life!" author="Lecturer Feedback" %}


## 4. Logo {#logo}
To use a logo in the `masthead` of your site. Ensure you have the images stored in `assets/images` Go to `config.yml` and add the url to your preferred image. 

## 5. Favicon {#favicon}
What is a favicon? To use one on your site, go to <a href="https://favicon.io/" target="_blank" rel="noopener noreferrer">Favicon.io</a> and generate a set of favicons. For now you can just upload the 32 x 32 size to `assets/images`. 

## 6. Single image - Use the `figure` include. Remember that it's good practice to include ALT text for accessibility. {#image}
{% include figure image_path="/assets/images/placeholder-2.png" alt="Game Jam screenshot" caption="This is a caption" %}

## 7. Gallery - A gallery is a good way to showcase some of the various components of your game. Remember to name your galery appropriately. Look at the `gallery` include to see the available keys. Gameplay Gallery - The content of the gallery is in the `head` of this page. Look at the `gallery` include for available keys.  {#gallery}
{% include gallery id="gallery_gameplay" layout="third" thumb_height="180px" %}

## 8. Second gallery in the same page - Make sure you reference the gallery id. {#second-gallery}
## Game Art Gallery
{% include gallery id="gallery_gameart" layout="third" thumb_height="180px" %}

## 9. Video - Look at the `video` include to see how it handles vidoes from different sources. Also be mindful to only extract and use the `video id`.  {#video}
Let's talk about the Rick Roll phenomena...
{% include video id="dQw4w9WgXcQ" provider="youtube" %}

## 10. Standard button - Look at the `button` include to see the available keys. {#standard-button}
{% include button
  url="/projects/"
  label="View All Projects"
  class="btn--primary"
%}

## 11. Call to Action (CTA) [Download button]. If you want to store downloadable information in your repo, you can use this CTA. Look at the `download` include to see the available keys. {#call-to-action-cta-button}

{% include download
  title="Download my Project Proposal"
  url="/assets/downloads/Project-proposal.pdf"
  button_label="Download Project Proposal"
  download="Project-proposal.pdf"
%}

## 12. Skills - The Skills content is in the `head` of this page. Look at the `skills` include for available keys. Use <a href="https://fontawesome.com/icons" target="_blank" rel="noopener noreferrer">Font Awesome</a> for icons. {#skills}
{% include skills skills=page.skills %}

## 13. Feature row - An excellent way to showcase projects or other hidden talents that you might have. Look at the `feature_row` include for available keys.  {#feature-row}
{% include feature_row %}

## 14. Embedded Google Form. If you are going to add a Contact form then we need to adjust some settings in Google. Ask me about this.  {#contact-form}
{% include google-form
  title="Contact Me"
  src="https://forms.gle/XsbApFoRjn7r24jy6"
  height="800"
%}



