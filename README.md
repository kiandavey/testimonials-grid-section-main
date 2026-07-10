# Frontend Mentor - Testimonials grid section solution

This is a solution to the [Testimonials grid section challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/testimonials-grid-section-Nnw6J7Un7). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [AI Collaboration](#ai-collaboration)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the site depending on their device's screen size

### Links

- Solution URL: [https://www.frontendmentor.io/solutions/testimonials-grid-section-built-with-css-grid-and-flexbox-Y81n](https://www.frontendmentor.io/solutions/testimonials-grid-section-built-with-css-grid-and-flexbox-Y81n)
- Live Site URL: [https://kiandavey.github.io/testimonials-grid-section/](https://kiandavey.github.io/testimonials-grid-section/)

## My process

### Built with

- Semantic HTML5 markup (including structural `<blockquote>` elements for text quotes)
- CSS custom properties (Variables)
- Flexbox (for mobile card stacking and interior content layouts)
- CSS Grid (for managing complex, staggered desktop grid tracks)
- Mobile-first responsive workflow
- Accessible typography with relative `rem` units

### What I learned

This challenge provided excellent experience mapping out an asymmetrical, asymmetric grid structure spanning a $4 \times 2$ track matrix. I learned how to combine `grid-column` span properties with strict coordinates to position floating rows cleanly, including forcing Kira's vertical card to span the entire height:

```html
<div class="card-container">
  <div class="card daniel">...</div>
  <div class="card jonathan">...</div>
  <div class="card jeanette">...</div>
  <div class="card patrick">...</div>
  <div class="card kira">...</div>
</div>
```
```css
@media (min-width: 68em) {
    .card-container {
        display: grid;
        grid-template-columns: repeat(4, 1fr);
        grid-template-rows: repeat(2, auto);
        gap: 1.875rem;
    }

    .daniel {
        grid-column: span 2;
    }

    .kira {
        grid-column: 4;
        grid-row: 1 / span 2;
    }

    .patrick {
        grid-column: 2 / span 2;
        grid-row: 2;
    }
}
```
I also leveled up my understanding of accessibility guidelines. By shifting absolute px font thresholds to native rem values, I ensured the page dynamically respects custom user text scaling preferences across different desktop and mobile browser configurations.

## Continued development
Moving forward, I want to keep prioritizing clean HTML structure and native semantic elements over generic generic generic tags. I also want to explore managing intricate layout overlays—like combining SVG background pattern graphics alongside responsive CSS grids—more efficiently without relying on extra presentation wrapper wrappers.

## AI Collaboration
Tools Used: Gemini

Usage Strategy: Assisted in establishing accessible typography frameworks, troubleshooting semantic tag structural implementations (specifically upgrading quote containers to blockquote), and calculating correct responsive media query constraints.

### Author
Frontend Mentor - @kiandavey