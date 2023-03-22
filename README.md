# FEM-Results-summary-component

This is a solution to the [Results summary component challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/results-summary-component-CE_K6s0maV). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Useful resources](#useful-resources)
- [Author](#author)

## Overview

### The challenge

Users should be able to:

- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![Live version of the project](/assets/images/Screenshot%202023-03-22%20112607.png)


### Link

- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- media-Queries workflow
- Mobile into Desktop view

### What I learned

I mainly focused on the css part of the project because of the simplicity of the Html, nothing to really worry about; With that being said, you can really just bring a lot with the css and I really enjoyed being able to create sa lot and be creative with it. 

Something to notice is data attributes to style items that are quiet the same but has different styling processes. I used it twice but its very useful and saves a lot of code.

For example :

```html
<div class="summary grid-flow" data-spacing="large">
  <div class="grid-flow"></div>
</div>
```
```css
.grid-flow {
    display: grid;
    align-content: start;
    gap: 1rem;
}

.grid-flow[data-spacing="large"] {
    gap: 2rem;
}
```

Also to handle the part of the color opacities that differ from one to another, still using the variables and the function "hsla()", and that with declaring the hsl values as variables instead of the function itself, and use "hsla()" whenever the opacity changes are needed.

Like so :

```css
:root {
--hsl-neutral-900 : 0, 0%, 100%;
}

.result-score {
color: hsla(var(--hsl-neutral-900), .5);
}
```

That helps when u need to adjust the color, u can just change the hsl values from the root variable without messing anything up, and not have to pass from alot of processing.

To end up with, is just a little additional tip to make a perfect sized circle with "aspect-ratio" :

```css
.result-score {
    /* ensure the perfect circle size */
    aspect-ratio: 1/1;
    border-radius: 50%;
}
```

### Useful resources

- [Detailed guide about css grid](https://css-tricks.com/snippets/css/complete-guide-grid/) - This helped me because I focused a lot on using grid for layouts. I really liked the process and the content is so useful.
- [Andy-Bell modern css resets](https://andy-bell.co.uk/a-modern-css-reset/) - This is an amazing article for css resets. I didn't used everything in there because it's a small project anyway, but its highly recommended to anyone that wants to know more about resets.

## Author

- Frontend Mentor - [@Simow03](https://www.frontendmentor.io/profile/Simow03)
