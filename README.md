# Frontend Mentor - Blog preview card solution

This is a solution to the [Blog preview card challenge on Frontend Mentor](https://www.frontendmentor.io/challenges/blog-preview-card-ckPaj01IcS). Frontend Mentor challenges help you improve your coding skills by building realistic projects.

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
<!-- - [Acknowledgments](#acknowledgments) -->

## Overview

This challenge is a perfect project for getting up to speed with HTML and CSS fundamentals, like HTML structure and the box model. The challenge is to build out this blog preview card and get it looking as close to the design as possible. You can use any tools you like to help you complete the challenge. In this project, I want to try new sass values for my styles.

### The challenge

Users should be able to:

- See hover and focus states for all interactive elements on the page
- Have a basic understanding of HTML and CSS

### Screenshot

![Site Preview](images/Screenshot%202023-12-27%20104323.png)

### Links

- Solution URL: [Add solution URL here](https://your-solution-url.com)
- Live Site URL: [Github Pages](https://pjiceskull.github.io/blog-preview-card-main/)

## My process

Before building the design, I set up my project directory and my npm scripts. I also take a look at the files found inside the zip file. These include the **assest** folder and the **styles-guide.md** file. Then after installing Sass, I created two Sass files to hold the websites' variables and fonts. In my **variables.scss** file I will be using the map value to handle the color values. Since the starter files include the fonts for the website I will import them locally.

The second thing I want to do before I begin working is identify each important in the design. The first thing I notice is the colors, yellow is used for the background and black is the color of the border and the text. The expectation is the text under **HTML & CSS foundations** where its font color is gray. There are other styles like the box’s border-radius and there’s a shadow behind the card.

The first thing I work on is the container for design. This container will hold the background color as well as the card component of the design. For the container, I will be using the main tag. I considered using the body tag for this purpose but I thought it’d be better to use landmark tags for readability. For the card component, I will be using the article tag as the container. I also used landmark tags for each element. For the hover states, I wanted this to look professional so I animated it using the transition property.

### Built with

- Semantic HTML5 markup
- CSS custom properties
  - Flexbox
  - Box-shadow
  - Border-radius
  - Transition
- [SCSS](https://sass-lang.com/) - Preprocessor Language for CSS
- [Visual Studio Code](https://code.visualstudio.com/) - Code Editor

### Planning

### What I learned

- Add transition property on the **parent element** instead of its **hover state** to animate after the hover state ends.

### Code I’m proud off

```scss
// Theme Colors
$Yellow: hsl(47, 88%, 63%);
$White: hsl(0, 0%, 100%);
$Grey: hsl(0, 0%, 50%);
$Black: hsl(0, 0%, 7%);

// palette
$colors: (
  "yellow": $Yellow,
  "white": $White,
  "grey": $Grey,
  "black": $Black,
);
```

```scss
article {
  background-color: map-get($map: $colors, $key: "white");
  max-width: 400px;
  min-height: 500px;
  border-radius: 25px;
  border: 1px solid map-get($map: $colors, $key: "black");
  padding: 25px;
  box-shadow: 7px 7px 0px 0px map-get($map: $colors, $key: "black");
  transition: 0.4s;
  &:hover {
    box-shadow: 17px 17px 0px 3px map-get($map: $colors, $key: "black");
  }
}
```

<!-- If you want more help with writing markdown, we'd recommend checking out [The Markdown Guide](https://www.markdownguide.org/) to learn more. -->

### Continued development

I think one area I want to improve in is type responsiveness. I tried to use the **clamp()** function in my project but I didn’t notice any changes.

### Useful resources

- [SASS Maps Tutorial](https://www.youtube.com/watch?v=La8wN7o-cL8&t=22s) - For helping me understand using the **Map** value in SASS.
- [Google Fonts](https://fonts.google.com/specimen/Figtree) - Font for Figtree.
- [W3Schools](https://www.w3schools.com/howto/howto_css_transition_hover.asp) - Transition on Hover
- [MDN Web Docs](https://developer.mozilla.org/en-US/docs/Web/CSS/::selection) - For changing the color of the highlighted text

## Author

- Website - [Pierce Issah](https://pjiceskull.github.io/WebPorfolio)
- Frontend Mentor - [@PJIceskull](https://www.frontendmentor.io/profile/PJIceskull)
- Twitter - [@Pierce24I](https://twitter.com/pierce24i)

<!-- ## Acknowledgments -->

<!-- This is where you can give a hat tip to anyone who helped you out on this project. Perhaps you worked in a team or got some inspiration from someone else's solution. This is the perfect place to give them some credit. -->
