# Frontend Mentor - Product preview card component solution

This is a solution to the [Product preview card component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/product-preview-card-component-GO7UmttRfa). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Frontend Mentor - Product preview card component solution](#frontend-mentor---product-preview-card-component-solution)
    - [Table of contents](#table-of-contents)
    - [Overview](#overview)
        - [The challenge](#the-challenge)
        - [Screenshot](#screenshot)
        - [Links](#links)
    - [My process](#my-process)
        - [Built with](#built-with)
        - [What I learned](#what-i-learned)
        - [Continued development](#continued-development)

## Overview

### The challenge

Users should be able to:

- View the optimal layout depending on their device's screen size
- See hover and focus states for interactive elements

### Screenshot

![](./screenshot-desktop.png)
![](./screenshot-mobile.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- Flexbox
- Mobile-first workflow

### What I learned

The layout change on desktop was the most difficult part of this challenge.
I used Flexbox on the card, so to change the layout so
the image was on the left,
all I needed to do was change the flex-direction to row.

I noticed in the desktop design image that the width of the card
was shared equally between the image and the text container.
At first, I thought I could just use Flexbox again, but
that turned out to be harder than what I eventually
came up with:

```css
@media screen and (min-width: 375px) {
  .product-card {
    border-radius: 0.5rem;
    flex-direction: row;
  }

  .thumbnail {
    content: url(./images/image-product-desktop.jpg);
    width: 50%;
    border-radius: 0.5rem 0 0 0.5rem;
  }

  .product-info {
    padding: 1.5rem;
    width: 50%;
  }
}
```

What I learned is that tools like Flexbox and Grid can
make things more simple, but they can also make things more
complicated. So, I think I should make it a habit 
to only use them if a more straightforward alternative doesn't exist.

### Continued development

One interesting issue I noticed was that the image was stretched
slightly when the width of the screen was about 375-530px. This
was when the card needed to shrink while still in desktop mode.
I am not entirely sure how to solve this, so it could be something
to look into.
