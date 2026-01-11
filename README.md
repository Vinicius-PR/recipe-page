# Frontend Mentor - Recipe page solution

This is my solution to the [Recipe page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/recipe-page-KiTsR8QQKm).

## Table of contents

- [Overview](#overview)
  - [The challenge](#the-challenge)
  - [Preview](#preview)
  - [Links](#links)
- [My process](#my-process)
  - [Built with](#built-with)
  - [What I learned](#what-i-learned)
- [Author](#author)


## Overview

### The challenge

This challenge was an easy one, focused on CSS and HTML only. One thing that was new to me was to change the list bullets, the numbers and spacing.

### Preview

![preview](/preview.jpg)

### Links

- Live Site URL: [Live site URL](https://recipe-page-beta-peach.vercel.app/)

## My process

### Built with

- Semantic HTML5 markup
- CSS3
- Flexbox

### What I learned

I learned a new way to customize list bullets and numbers. The design required different spacing than the default browser styles, so I used **position: relative** and **position: absolute** with the **::before** pseudo-element. Check the code below.

```css
ul, ol {
  list-style-position: inside;
  list-style: none;
  color: var(--stone-600);
}

.preparation-list,
.ingredient-list {
  padding-left: var(--spacing-100);
}

.preparation-list li,
.ingredient-list li {
  position: relative;
  padding-left: var(--spacing-400);
}

.preparation-list li::before,
.ingredient-list li::before{
  content: "";
  width: 4px;
  height: 4px;
  background-color: var(--rose-800);
  border-radius: 50%;
  position: absolute;
  left: 0;
  top: 50%;
  transform: translateY(-50%);
}
```

## Author

- Frontend Mentor - [@Vinicius-PR](https://www.frontendmentor.io/profile/Vinicius-PR)
- Linkedin - [@Vinicius](https://www.linkedin.com/in/vinicius-paula-resende/)
