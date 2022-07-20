# Index

[Home](./README.md)  
[Responsive Design](#responsive-design)  
[Planning](#planning)
- [Media Querries](#media-querries)
[Fluid Grids](#fluid-grids)

## [Responsive Design](https://developer.mozilla.org/en-US/docs/Learn/CSS/CSS_layout/Responsive_Design)

A set of practices that allows web pages to alter their layout and appearance to suit different screen widths,
resolutions, etc. It is an idea that changed the way we design for a multi-device web.
The most obvious factor here is screen size, but there are other factors as well, including the pixel density of the display and whether it supports touch. Responsive Design Mode gives you a simple way to simulate these factors, to test how your website will look and behave on different devices.

- [Responsive Design: Building Blocks](https://developer.mozilla.org/en-US/docs/Web/Progressive_web_apps/Responsive/responsive_design_building_blocks)

<p align="center">
  **A short video from Raddy discussing the basics of responsive design.**
</p>

<p align="center">
<iframe width="560" height="315" src="https://www.youtube.com/embed/vZB1s8J6dhY" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture" allowfullscreen></iframe>
</p>

## Planning

- Plan how things will look Know the basic look and layout of your page before you do anything else.
  - Mobile
  - Tablet
  - Desktop
- [inVision](./#prototyping) Free Whiteboarding
- [Wireframe: Layout Design Prototyping](./links/#prototyping)

1. Start with base styles first.
2. Then plan out platform views i.e. Desktop, Tablet, Phone, ect. Use media querries to target different sized device screens.  Less is more, only use what you need. 3 media querries is usually enough.

### Media Querries

```css
/* Extra small devices (phones, 600px and down) */
@media only screen and (max-width: 600px) {...}

/* Small devices (portrait tablets and large phones, 600px and up) */
@media only screen and (min-width: 600px) {...}

/* Medium devices (landscape tablets, 768px and up) */
@media only screen and (min-width: 768px) {...}

/* Large devices (laptops/desktops, 992px and up) */
@media only screen and (min-width: 992px) {...}

/* Extra large devices (large laptops and desktops, 1200px and up) */
@media only screen and (min-width: 1200px) {...} 

@media only screen and (orientation: portrait)
@media only screen and (orientation: landscape)

/* If the screen size is 600px wide or less, hide the element */
@media only screen and (max-width: 600px) {
  div.example {
    display: none;
  }
}
```

[Source: W3schools](https://www.w3schools.com/css/css_rwd_mediaqueries.asp)

## Fluid Grids

- [CSS Grid @ W3Schools](https://www.w3schools.com/css/css_grid.asp)
  - The CSS Grid Layout Module offers a grid-based layout system, with rows and columns, making it easier to design web pages without having to use floats and positioning.
- [CSS Grid @ MDN](https://developer.mozilla.org/en-US/docs/Web/CSS/grid)
  - he grid CSS property is a shorthand property that sets all of the explicit and implicit grid properties in a single declaration. Using grid you specify one axis using [grid-template-rows](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-rows) or [grid-template-columns](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-template-columns), you then specify how content should auto-repeat in the other axis using the implicit grid properties: [grid-auto-rows](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-rows), [grid-auto-columns](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-columns), and [grid-auto-flow](https://developer.mozilla.org/en-US/docs/Web/CSS/grid-auto-flow).

- An intro to [Flexbox](https://web.dev/learn/css/flexbox/)
  - The Flexible Box Layout Model (flexbox) is a layout model designed for one-dimensional content. It excels at taking a bunch of items which have different sizes, and returning the best layout for those items.
- [Flex Properties](https://www.w3schools.com/cssref/css3_pr_flex.asp)
  - flex-basis
  - flex-direction
  - flex-flow
  - flex-grow
  - flex-shrink
  - flex-wrap

```html
<html>
<head>
<style>
.flex-container {
  display: flex;
  flex-wrap: nowrap;
  background-color: DodgerBlue;
}

.flex-container > div {
  background-color: #f1f1f1;
  width: 100px;
  margin: 10px;
  text-align: center;
  line-height: 75px;
  font-size: 30px;
}
</style>
</head>
<body>
  <h1>Flexible Boxes</h1>

  <div class="flex-container">
    <div>1</div>
    <div>2</div>
    <div>3</div>  
    <div>4</div>
    <div>5</div>
    <div>6</div>  
    <div>7</div>
    <div>8</div>
  </div>

  <p>Try to resize the browser window.</p>
  <p>A container with "flex-wrap: nowrap;" will never wrap its items.</p>
  <p><strong>Note:</strong> Flexbox is not supported in Internet Explorer 10 or earlier versions.</p>
</body>
</html>
```

```html
<html>
<head>
<style>
.item1 { grid-area: header; }
.item2 { grid-area: menu; }
.item3 { grid-area: main; }
.item4 { grid-area: right; }
.item5 { grid-area: footer; }

.grid-container {
  display: grid;
  grid-template-areas:
    'header header header header header header'
    'menu main main main right right'
    'menu footer footer footer footer footer';
  gap: 10px;
  background-color: #2196F3;
  padding: 10px;
}

.grid-container > div {
  background-color: rgba(255, 255, 255, 0.8);
  text-align: center;
  padding: 20px 0;
  font-size: 30px;
}
</style>
</head>
  <body>
    <h1>Grid Layout</h1>

    <p>This grid layout contains six columns and three rows:</p>

    <div class="grid-container">
      <div class="item1">Header</div>
      <div class="item2">Menu</div>
      <div class="item3">Main</div>  
      <div class="item4">Right</div>
      <div class="item5">Footer</div>
    </div>
  </body>
</html>
```

[Back to Top](#Index)
