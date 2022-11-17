# Frontend Mentor - CHALLENGE

This is a solution to the [Blogr landing page challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blogr-landing-page-EX2RLAApP). Frontend Mentor challenges help you improve your coding skills by building realistic projects. 

## Table of contents

- [Overview](#overview)
    - [The challenge](#the-challenge)
    - [Extra challenge](#extra-challenge)
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

- View the optimal layout for the site depending on their device's screen size
- See hover states for all interactive elements on the page

### Extra challenge

As an extra challenge I will do the following things:

- Add a color theme switcher, with about five themes, that is persisted in `localStorage`.
- Add smooth animations for better interactivity on the hero, images and buttons.
- Make the game accessible according to WCAG 2.1 standards, things like color contrast, clear element focus and the correct screen reader contexts.

### Screenshot

![social-preview-image](https://user-images.githubusercontent.com/3909046/202434010-6024a25e-2567-4455-ae20-fb18eaadd7c1.png)

### Links

- [Solution URL](https://www.frontendmentor.io/solutions/astro-wcag-accessibility-theme-switcher-intersectionobserver-api-46NWfLGB-z)
- [Live Site URL](https://markteekman.github.io/blogr-landing-page/)

## My process

### Built with

- Semantic HTML5 markup
- CSS custom properties
- Flexbox
- CSS Grid
- WCAG 2.1 best practices
- CSS Animations
- Vanilla JavaScript
- Tailwind CSS
- [Astro](https://astro.build) - Astro Static Site Generator
- [Frontend Mentor Challenge Starter](https://github.com/markteekman/frontend-mentor-challenge-starter) - My own starter template for Frontend Mentor Challenges

### What I learned

- How the `<picture>` element works. I've never used it before, but found a great use case for it in this challenge. I learned that you can use it to load different images depending on the screen size using the `<source>` tag and the `srcset` attribute. This is very useful for responsive images.

```html
<picture>
  <source media="(min-width: 768px)" srcset="/image-header-desktop.jpg" />
  <img src="/image-header-mobile.jpg" alt="" />
</picture>
```

- How to build a [Theme Switcher](https://github.com/markteekman/blogr-landing-page/blob/main/src/components/ThemeSwitcher.astro) component with CSS variables. This was something I wanted to do for a long time now and this challenge was great for that, seeing as it has a nice orange theme going through the hero and the images. I used the `localStorage` API to persist the theme in the browser, so it will stay the same when you refresh the page. The styles are saved in Custom Properties, which are then used in the CSS. This way you can easily change the theme by changing the value of the Custom Property.

- How to change the color of the SVG as an image src with the `filter` property. This is something that has brought the Theme Switcher to the next level. I used the `filter` property to change the color of the SVGs in the Theme Switcher. This way I can use the same SVG for all the themes and just change the color. This is a great way to keep the SVGs small and not have to load multiple SVGs for each theme.

```css
img,
svg {
  filter: invert(0%) sepia(0%) saturate(100%) hue-rotate(210deg) brightness(100%) contrast(100%);
}
```

- How to make a magic sparkling text by following the tutorial by [Hyperplexed](https://www.youtube.com/watch?v=yu0Cm4BqQv0). This was a lot of fun to do and I learned more about using JavaScript to create random animations.

- I already knew about `<hgroup>` but in this project I started using it more extensively. The `<hgroup>` element represents a heading and related content. It groups a single `<h1>-<h6>` element with one or more `<p>` tags. 

### Continued development

- It would be cool to add a Dark Mode to the Theme Switcher. It would require a bit of extra work and extra Custom Properties, but it would be a nice addition to the Theme Switcher.

### Useful resources

[Hyperplexed YouTube channel](https://www.youtube.com/@Hyperplexed) - This is where I learned how to make the magic sparkling text. There are more useful videos on this channel, so I recommend checking it out.

## Author

- [Personal Website](https://www.markteekman.nl)
- [Frontend Mentor Profile](https://www.frontendmentor.io/profile/markteekman)
- [LinkedIn Profile](https://nl.linkedin.com/in/markteekman)
- [Twitter Profile](https://twitter.com/MarkTeekman)
- [GitHub Repositories](https://github.com/markteekman)
- [NPM Packages](https://www.npmjs.com/~markteekman)
- [CodePen Creations](https://codepen.io/markteekman)
