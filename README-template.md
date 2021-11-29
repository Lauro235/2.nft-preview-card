# Frontend Mentor - NFT preview card component solution

This is a solution to the [NFT preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/nft-preview-card-component-SbdUL_w0U). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover states for interactive elements

### Screenshot

![./nft-screenshot.png](./screenshot.jpg)

### Links

- Solution URL: [https://github.com/Lauro235/2.nft-preview-card](https://your-solution-url.com)
- Live Site URL: [https://codepen.io/Laurie312/full/PoKrYLg](https://your-live-site-url.com)

## My process

I blitzed through the main design as quickly as I could. Starting on the mobile version first. It's often fairly easy to scale upwards to desktop size. I actually almost prematurely submitted, before realising I had forgotten the hover/focus states. I clearly laid out my CSS which I learnt from seeing how John Smilga lays his CSS out.

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- Mobile-first workflow

### What I learned

In this project I want to thank Grace from the frontend slack community who guided me through, when I lost my balance a little bit. While I had intuited that the eye on hover should probably be added with the pseudo element ::after, Grace was the one that actually showed me that you COULD use pseudo elements and pseudo classes together. It turns out this doesn't break css!

I also looked into how to better structure my css and how to use variables to save whole font values. Ie not just the family, but weight, size etc all in one variable. This is really powerful especially in this kind of setting, where you're given a design spec to follow by sight.

```html
      <a href="/" class="hero-image-container">
        <img class="hero-image" src="https://i.postimg.cc/NfR2yhNs/image-equilibrium.jpg" alt="Spinning glass cube"/>
      </a>
```
```css

<!-- Example of variable held in :root -->

    --var-para: normal normal 300 1em/1.55em 'Outfit', sans-serif;
    
<!-- The Anchor and the Eye -->

.hero-image-container::after {
    content: '';
    background-image: url("https://i.postimg.cc/9MtT4GZY/view.png");
    background-position: center;
    background-repeat: no-repeat;
    background-size: 5rem;
    background-color: hsla(178, 100%, 50%, 0.3);
    width: 100%;
    height: 100%;
    border-radius: 1rem;
    position: absolute;
    top: 0;
    left: 0;
    display: block;
    z-index: 2;
    opacity: 0;
    transition: opacity 0.3s ease-out;
}

.hero-image-container:hover::after {
  opacity: 1;
}
```

### Continued development

What I've found useful about using Frontend Mentor is that the design is made for you. This working method of 'copy what you see' is really intuitive and helps me get into a flow. In my future learning, this could go hand in hand with making wireframe designs. I'd like to be able to knock out super quick designs in a kind of blocky way. So that I can have this visual thing to look at.

## Author

- Frontend Mentor - [@Lauro235](https://www.frontendmentor.io/profile/Lauro235)
- Twitter - [@Lauro235](https://twitter.com/Lauro235)

## Acknowledgments

Grace from the frontend mentor slack community. I salute you!
