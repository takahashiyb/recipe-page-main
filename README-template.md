# Frontend Mentor - Recipe page solution

This is a solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Screenshot](#screenshot)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
  - [Continued development](#continued-development)
  - [Useful resources](#useful-resources)
- [Author](#author)
- [Acknowledgments](#acknowledgments)

**Note: Delete this note and update the table of contents based on what sections you keep.**

## Overview

### Screenshot

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://your-live-site-url.com)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- Lists and tables
- Mobile-first workflow

### What I learned

I learned that lists are actually not as straight forward as I thought. When I did it initially, I thought it was already fine, but when I checked with Copilot regarding the quality of my HTML without assistance, I found that there were many parts that were not up to industry standards. I thought that divs could exist within lists but that was not the case, so I had to adjust and learn more about them.

On major part of lists I learned is, that it is better to use ::before pseudo-class and ditch the ::marker pseudo-class especially when you need to customize its position.

```css
.preparation-time-section li {
  display: flex;
  list-style-type: none; /*Explitly done but the display:flex; removes it without this*/
}

.preparation-time-section li::before {
  content: "•";
  align-self: center; /* positions the marker */
  /* Enter the styling of the marker here*/
}
```

I also learned of counters within css, which I thought was a JS only thing.

```css
ol {
  counter-reset: step;
}

ol li::before {
  counter-increment: step;
  content: counter(step) ".";
}
```

When working with text that have different styling, but you want it within the same line/paragraph, then just use span and enclose that text with a different format with elements such as strong or another span with a class.

This was especially relevant when aligning the list marker to the center of a word-wrapped text, and the text should word wrap across the entire text but not the marker. This might be easier done with divs but I decided to keep it machine readable, so I used only valid elements within that constraint.

```html
<li>
  <span class="text-preset-four"
    ><strong class="label text-preset-four-bold">Total</strong>Approximately 10
    minutes</span
  >
</li>
```

### Continued development

I would like to learn more about HTML tags and how to keep them machine readable.

Also, I would maintain adding about fonts until I actually learn about them. For accountability.

### Useful resources

## Author

- Frontend Mentor - [@takahashiyb](https://www.frontendmentor.io/profile/yourusername)

## Acknowledgments
