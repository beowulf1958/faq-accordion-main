# Frontend Mentor - FAQ accordion solution

This is a solution to the [FAQ accordion challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/faq-accordion-wyfFdeBwBz). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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

## Overview

### The challenge

Users should be able to:

- Hide/Show the answer to a question when the question is clicked
- Navigate the questions and hide/show answers using keyboard navigation alone
- View the optimal layout for the interface depending on their device's screen size
- See hover and focus states for all interactive elements on the page

### Screenshot

![Screenshot](./app/assets/images/Screenshot%202023-12-06%20FAQ%20accordion.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Add live site URL here](https://papaya-cocada-26f35e.netlify.app/)

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- [Sass](https://sass-lang.com/) - Sass / scss

### What I learned

This challenge is similar to another accordian challenge that I had already completed. On that challenge I used <details> and wanted to try using input:radio button. At the outset, the challenges appeared to be swapping out the svg and making it accessible.

I built the project with radio buttons, and figured out how swap out the svg with ::after. However, although the input would focus, I could not get it to open.

Went back to <details>. The focus worked, and it would open with spacebar, but struggled with the ::after. Finally worked it out below:

```css
summary:hover,
summary:active,
summary:focus {
  color: var(--clr-accent);
  cursor: pointer;
}
summary::after {
  content: url(./app/assets/images/icon-plus.svg);
}
details[open] summary::after {
  content: url(./app/assets/images/icon-minus.svg);
}
```

### Continued development

Now that I have learned a bit about accessibilty, will look to see if my challenges in the future are accessible.

Need to figure out what went wrong with the input buttons

### Useful resources

- [Resource 1](https://www.smashingmagazine.com/2022/11/guide-keyboard-accessibility-html-css-part1/) - This helped me get started with accessiblity. I learned summary is focusable, and elsewhere learned about tabindex.
- [Resource 2](https://stackoverflow.com/questions/56758098/how-to-position-detail-marker-to-come-after-summary) - This is an amazing article which helped me finally switch svg when details is open. I'd recommend it to anyone still learning this concept.

## Author

- Frontend Mentor - [@beowulf1958](https://www.frontendmentor.io/profile/beowulf1958)
