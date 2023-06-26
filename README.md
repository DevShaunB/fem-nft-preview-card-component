# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [Reference](#reference)
  - [Font](#font)
  - [Color](#color)
  - [Typography](#typography)
- [Run Locally](#run-locally)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![NFT preview card component desktop screenshot](https://devshaunb.github.io/fem-nft-preview-card-component/screenshots/desktop.png)

![NFT preview card component mobile screenshot](https://devshaunb.github.io/fem-nft-preview-card-component/screenshots/mobile.png)

### Links

- Live Site URL: [https://devshaunb.github.io/fem-nft-preview-card-component/](https://devshaunb.github.io/fem-nft-preview-card-component/)

## Reference

### Font

- Family: [Outfit](https://fonts.google.com/specimen/Outfit)
- Weights: 300, 400, 600

### Colors

#### Primary

- ![hsl(215, 51%, 70%)](https://via.placeholder.com/10/8bacda?text=+) `Soft blue: hsl(215, 51%, 70%)`
- ![hsl(178, 100%, 50%)](https://via.placeholder.com/10/00fff7?text=+) `Cyan: hsl(178, 100%, 50%)`

#### Neutral

- ![hsl(217, 54%, 11%)](https://via.placeholder.com/10/0d192b?text=+) `Very dark blue (main BG): hsl(217, 54%, 11%)`
- ![hsl(216, 50%, 16%)](https://via.placeholder.com/10/14253d?text=+) `Very dark blue (card BG): hsl(216, 50%, 16%)`
- ![hsl(215, 32%, 27%)](https://via.placeholder.com/10/2f415b?text=+) `Very dark blue (line): hsl(215, 32%, 27%)`
- ![hsl(0, 0%, 100%)](https://via.placeholder.com/10/ffffff?text=+) `White: hsl(0, 0%, 100%)`

### Typography

#### Body Copy

- Font size (paragraph): 18px

## Run Locally

Clone the project

```bash
  git clone https://github.com/DevShaunB/fem-nft-preview-card-component.git
```

Go to the project directory

```bash
  cd fem-nft-preview-card-component/
```

Run `index.html`

```bash
  <browsername> index.html
```

E.g.

```bash
  firefox index.html
```

```bash
  google-chrome index.html
```

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Mobile-first workflow
- Custom utility classes (like [TailwindCSS](https://tailwindcss.com/))

### What I learned

- using BEM (Block, Element, Modifier) for naming CSS classes

```html
<div class="nft-card flex flex-center">
  <div class="nft-card__text">
    <h2 class="nft-card__title">Equilibrium #3429</h2>
    <p class="nft-card__desc">Our Equilibrium ... calm.</p>
  </div>
</div>
```

- working with pseudo-elements

```css
.nft-card__img-wrapper::before {
  content: '';
  background-color: hsl(var(--clr-cyan-400) / 0.5);
  position: absolute;
  inset: 0;
}
```

- creating and using CSS custom properties

```css
:root {
  --clr-blue-900: 217 54% 11%;
}

.nft-card__img-wrapper:hover::before {
  background-color: hsl(var(--clr-cyan-400) / 0.5);
}
```

- creating and using custom utility classes (like [TailwindCSS](https://tailwindcss.com/))

```html
<body class="flex flex-center bg-blue-900">
  <!-- rest of the code -->
</body>
```

```css
.flex {
  display: flex;
}

.flex-center {
  align-items: center;
  justify-content: center;
}

.bg-blue-900 {
  background-color: hsl(var(--clr-blue-900));
}
```

- center element with `position: absolute`

```css
.nft-card__img-wrapper {
  position: relative;
}

.nft-card__img-wrapper:hover::after {
  content: url('./images/icon-view.svg');
  position: absolute;
  top: 50%;
  left: 50%;
  transform: translate(-50%, -50%);
}
```

### Useful resources

- [How to plan your HTML](https://fedmentor.dev/posts/html-plan-product-preview/) - This helped me make my HTML efficient and easy to maintain. It also helped by drawing focus to accessibility.

- [Why font-size must NEVER be in pixels](https://fedmentor.dev/posts/font-size-px/) - This helped me understand why I must avoid pixels for modern front-end development. It also introduced me to the pitfalls to look for when working with responsive units.

## Author

- Frontend Mentor - [@DevShaunB](https://www.frontendmentor.io/profile/DevShaunB)
- Twitter - [@DevShaunB](https://www.twitter.com/DevShaunB)

## Acknowledgments

- [NFT preview card component](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U) by [Frontend Mentor](https://www.frontendmentor.io/)

- [FED Mentor](https://fedmentor.dev/)
