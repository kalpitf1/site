---
layout: ../layouts/BlogPost.astro
title: Breakfast Bowls
slug: breakfast-bowls
description: Made a website showcasing some breakfast bowls I made
tags:
  - technical
added: 2024-08-30T17:48:43.468Z
---

So, I made a website using plain HTML, CSS, and JS. The website showcases some oatmeal bowls that I have made in the past. A design doc that I followed was this screenshot I took of a post that I saw on Instagram (painful, I know). Source is on [Github](https://github.com/kalpitf1/recipes) and deployed using Netlify on [breakfastbowls.netlify.app/](https://breakfastbowls.netlify.app/).

Cool things learnt on the way:

* flexbox is such a friend when you want to arrange divs relative to each other in a space. It was helpful when setting up a responsive layout but especially cool in the scenario on mobile screens where I wanted some image container (think of it as a footer) to have a fixed height and the title and description container (think of it as page content) that is of variable height and should occupy the remaining space on the viewport. Source: [this stackoverflow post](https://stackoverflow.com/questions/25098042/fill-remaining-vertical-space-with-css-using-displayflex)
* Modern image formats like WebP offer much better image compression than jpeg or png. Can use them inside the `<picture>` element with multiple possible sources like WebP, jpeg, png, etc. and the first available source is picked on supported browsers and use a fallback image on older browsers.
* Preloading images for browser caching leading to slightly slower initial page load can be a valid tradeoff for a quicker loading and smoother UX when user needs to cycle through large images.
* CSS animations are fun - [make your own using @keyframes](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_animations/Using_CSS_animations#defining_an_animation_sequence_using_keyframes) or use a library like [Animate.css](https://animate.style/https://animate.style/) (haven't played around with this so lemme know how you like it).
* In CSS, you can make a background color darker (similarly lighter) by applying a background image of a constant linear-gradient of black with some alpha value. I needed this in the scenario where I had dynamically set background colors but I wanted to programmatically set all colors to a darker color for better contrast-ratio of my light text to background.

```css
body {
  background-color: #E57D3A;  // set dynamically in a script in my case
  background-image: linear-gradient(to bottom, rgba(0, 0, 0, 0.4) 10%, rgba(0, 0, 0, 0.4));
}
```

That's all for now. Hope this helps!
