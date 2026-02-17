# Complete CSS Guide: From Basics to Advanced

## 1. What is CSS?

CSS (Cascading Style Sheets) is a stylesheet language used to describe the presentation of HTML documents. It controls colors, layouts, fonts, and overall visual appearance.  
**Three Ways to Add CSS:**

```css
/* 1. External CSS (Best Practice) */
<!-- In HTML <head> -->
<link rel="stylesheet" href="styles.css">

/* 2. Internal CSS */
<style>
    body { background-color: lightblue; }
</style>

/* 3. Inline CSS (Avoid when possible) */
<p style="color: red; font-size: 16px;">Hello</p>
```

## 2. CSS Selectors - Detailed Guide
**Basic Selectors:**
```css
/* Element Selector */
p { color: blue; }

/* Class Selector */
.button { background-color: green; }

/* ID Selector */
#header { font-size: 24px; }

/* Universal Selector */
* { margin: 0; padding: 0; }
```
**Combinator Selectors:**
```css

/* Descendant Selector (space) */
div p { color: red; }  /* All p inside div */

/* Child Selector (>) */
div > p { color: red; }  /* Direct children only */

/* Adjacent Sibling (+) */
h1 + p { margin-top: 0; }  /* p immediately after h1 */

/* General Sibling (~) */
h1 ~ p { color: gray; }  /* All p after h1 */
```
**Attribute Selectors:**
```css

input[type="text"] { border: 1px solid gray; }
a[href^="https"] { color: green; }  /* Starts with */
a[href$=".pdf"] { color: red; }     /* Ends with */
a[href*="google"] { color: blue; }  /* Contains */
```
**Pseudo-classes:**
```css

/* Dynamic States */
a:hover { color: orange; }
a:active { color: red; }
a:visited { color: purple; }
input:focus { outline: 2px solid blue; }

/* Structural */
li:first-child { font-weight: bold; }
li:last-child { border-bottom: none; }
li:nth-child(odd) { background: #f2f2f2; }
li:nth-child(3n+1) { color: red; }  /* Every 3rd starting from 1 */

/* Form States */
input:disabled { background: #eee; }
input:checked { box-shadow: 0 0 3px green; }
input:required { border-color: red; }
```
**Pseudo-elements:**
```css

p::first-line { font-weight: bold; }
p::first-letter { font-size: 200%; }
::selection { background: yellow; }

/* Content Insertion */
.element::before { 
    content: "→ ";
    color: blue;
}
.element::after { 
    content: " ←";
    color: red;
}

```
## 3. Colors in CSS
**Color Systems:**

```css
/* Named Colors */
color: red; color: tomato; color: rebeccapurple;  /* 147 named colors */

/* Hexadecimal */
color: #FF0000;      /* Red */
color: #F00;         /* Short form (same as #FF0000) */
color: #FF000080;    /* With alpha (transparency) */

/* RGB/RGBA */
color: rgb(255, 0, 0);
color: rgba(255, 0, 0, 0.5);  /* 0.5 = 50% opacity */

/* HSL/HSLA (Hue, Saturation, Lightness) */
color: hsl(0, 100%, 50%);           /* Red */
color: hsla(240, 100%, 50%, 0.3);   /* Blue with opacity */

/* Modern Color Formats */
color: color(display-p3 1 0 0);     /* Wide gamut colors */
color: lch(50% 100 30);             /* Perceptually uniform */
```

## 4. Typography & Text Properties
**Font Properties:**
```css

body {
    /* Font Family with Fallbacks */
    font-family: 'Helvetica', Arial, sans-serif;
    
    /* Font Size - Different Units */
    font-size: 16px;      /* Absolute */
    font-size: 1.2em;     /* Relative to parent */
    font-size: 1.2rem;    /* Relative to root element */
    font-size: 100%;      /* Percentage */
    font-size: 2vw;       /* Viewport width */
    
    /* Font Weight */
    font-weight: normal;  /* 400 */
    font-weight: bold;    /* 700 */
    font-weight: 300;     /* Light */
    font-weight: 900;     /* Black */
    
    /* Font Style */
    font-style: italic;
    font-style: oblique 10deg;
    
    /* Font Variant */
    font-variant: small-caps;
    
    /* Shorthand (order: style weight size/line-height family) */
    font: italic 700 16px/1.5 'Arial', sans-serif;
}
```
**Text Properties:**
```css

p {
    /* Alignment */
    text-align: left | right | center | justify;
    
    /* Decoration */
    text-decoration: underline;
    text-decoration: underline wavy red 2px;  /* Style, color, thickness */
    
    /* Transform */
    text-transform: uppercase | lowercase | capitalize;
    
    /* Spacing */
    letter-spacing: 2px;        /* Character spacing */
    word-spacing: 5px;          /* Word spacing */
    line-height: 1.6;           /* Unitless multiplier */
    
    /* Indentation */
    text-indent: 30px;
    
    /* Shadow */
    text-shadow: 2px 2px 4px rgba(0,0,0,0.3);
    /* Multiple shadows */
    text-shadow: 1px 1px 2px black, 0 0 1em blue;
    
    /* Wrapping */
    white-space: nowrap;        /* No wrap */
    word-wrap: break-word;      /* Break long words */
    word-break: break-all;      /* Break anywhere */
    
    /* Advanced */
    text-overflow: ellipsis;    /* Show ... for overflow */
    hyphens: auto;              /* Automatic hyphenation */
}
```
## 5. Box Model - Deep Dive
**Box Model Components:**
```css

.box {
    /* Content */
    width: 300px;
    height: 200px;
    min-width: 200px;
    max-width: 500px;
    
    /* Padding (Inside border) */
    padding-top: 10px;
    padding-right: 20px;
    padding-bottom: 10px;
    padding-left: 20px;
    /* Shorthand: top right bottom left */
    padding: 10px 20px 10px 20px;
    padding: 10px 20px;        /* top/bottom left/right */
    padding: 10px;              /* all sides */
    
    /* Border */
    border-width: 2px;
    border-style: solid | dashed | dotted | double | groove | ridge | inset | outset;
    border-color: black;
    /* Shorthand */
    border: 2px solid black;
    border-top: 3px dashed red;
    
    /* Border Radius */
    border-radius: 5px;
    border-radius: 10px 5px;    /* top-left/bottom-right top-right/bottom-left */
    border-radius: 50%;          /* Circle */
    
    /* Margin (Outside border) */
    margin: 10px 20px;
    margin: 0 auto;              /* Center horizontally */
    margin-top: -10px;           /* Negative margins allowed */
    
    /* Box Sizing */
    box-sizing: content-box;     /* Width excludes padding/border */
    box-sizing: border-box;      /* Width includes padding/border (recommended) */
}
```
**Box Model Visual Example:**
```css

/* Total width calculation */
.element {
    width: 300px;
    padding: 20px;
    border: 5px solid black;
    margin: 10px;
    
    /* content-box: total = 300 + 40 + 10 = 350px */
    /* border-box:  total = 300px (padding+border included) */
}
```
## 6. Display & Positioning
**Display Property:**
```css

.display-examples {
    display: block;           /* Takes full width, new line */
    display: inline;          /* Only as wide as content */
    display: inline-block;    /* Inline but can set width/height */
    display: none;            /* Completely hidden */
    display: flex;            /* Flexbox container */
    display: grid;            /* Grid container */
    display: table;           /* Table layout */
    display: list-item;       /* List behavior */
}
```
**Positioning Systems:**
```css

.positioning {
    /* Static (default) */
    position: static;
    
    /* Relative - relative to normal position */
    position: relative;
    top: 20px;
    left: 30px;
    
    /* Absolute - relative to nearest positioned ancestor */
    position: absolute;
    top: 0;
    right: 0;
    
    /* Fixed - relative to viewport */
    position: fixed;
    bottom: 10px;
    right: 10px;
    
    /* Sticky - hybrid relative/fixed */
    position: sticky;
    top: 0;
}
```
**Z-Index & Stacking Context:**
```css

.layer1 { z-index: 1; }      /* Lower number = lower layer */
.layer2 { z-index: 100; }    /* Higher number = on top */
.layer3 { z-index: auto; }    /* Default, follows DOM order */

/* Creates new stacking context */
.transform-context {
    transform: scale(1);
    opacity: 0.99;
    position: relative;
    z-index: 0;
}
```
## 7. Flexbox - Complete Guide
**Flex Container Properties:**
```css

.container {
    display: flex;            /* or inline-flex */
    
    /* Direction */
    flex-direction: row;                /* Default */
    flex-direction: row-reverse;        /* Right to left */
    flex-direction: column;             /* Top to bottom */
    flex-direction: column-reverse;     /* Bottom to top */
    
    /* Wrapping */
    flex-wrap: nowrap;        /* Default - all on one line */
    flex-wrap: wrap;          /* Multi-line */
    flex-wrap: wrap-reverse;
    
    /* Shorthand for direction and wrap */
    flex-flow: row wrap;
    
    /* Main Axis Alignment */
    justify-content: flex-start;        /* Default */
    justify-content: flex-end;          /* Align to end */
    justify-content: center;            /* Center */
    justify-content: space-between;     /* Equal space between */
    justify-content: space-around;      /* Space around items */
    justify-content: space-evenly;      /* Equal space around all */
    
    /* Cross Axis Alignment */
    align-items: stretch;               /* Default */
    align-items: flex-start;            /* Top */
    align-items: flex-end;              /* Bottom */
    align-items: center;                /* Middle */
    align-items: baseline;              /* Align by text baseline */
    
    /* Multi-line Cross Axis Alignment */
    align-content: stretch;             /* Default */
    align-content: flex-start;          /* Lines at start */
    align-content: flex-end;            /* Lines at end */
    align-content: center;              /* Lines centered */
    align-content: space-between;       /* Equal space between lines */
    
    /* Gap (Spacing) */
    gap: 10px;                          /* Both row and column gap */
    row-gap: 20px;                      /* Row gap only */
    column-gap: 15px;                   /* Column gap only */
}
```
**Flex Item Properties:**
```css

.item {
    /* Order */
    order: 2;                 /* Default 0, can be negative */
    
    /* Growth - How much item can grow */
    flex-grow: 1;             /* 0 = don't grow, 1+ = grow proportionally */
    
    /* Shrink - How much item can shrink */
    flex-shrink: 1;           /* 0 = don't shrink */
    
    /* Basis - Initial size before growing/shrinking */
    flex-basis: auto;         /* Default - based on content */
    flex-basis: 200px;        /* Fixed starting size */
    flex-basis: 30%;          /* Percentage of container */
    
    /* Shorthand: grow shrink basis */
    flex: 1 1 auto;           /* Common pattern */
    flex: 1;                  /* Equivalent to 1 1 0 */
    flex: 0 1 auto;           /* Default */
    
    /* Individual Alignment (overrides align-items) */
    align-self: auto;         /* Default - inherit from container */
    align-self: flex-start;
    align-self: flex-end;
    align-self: center;
    align-self: stretch;
}
```
**Flexbox Examples:**
```css

/* Perfect Centering */
.center-container {
    display: flex;
    justify-content: center;
    align-items: center;
    height: 100vh;
}

/* Holy Grail Layout */
.holy-grail {
    display: flex;
    flex-direction: column;
    min-height: 100vh;
}

.holy-grail > main {
    display: flex;
    flex: 1;
}

.holy-grail > main > article {
    flex: 1;
}

.holy-grail > main > nav {
    order: -1;
    width: 200px;
}

.holy-grail > main > aside {
    width: 200px;
}

/* Responsive Navigation */
.navbar {
    display: flex;
    flex-wrap: wrap;
    justify-content: space-between;
    align-items: center;
}

.nav-links {
    display: flex;
    gap: 20px;
    flex-wrap: wrap;
}
```
## 8. CSS Grid - Complete Guide
**Grid Container Properties:**
```css

.grid-container {
    display: grid;            /* or inline-grid */
    
    /* Defining Columns */
    grid-template-columns: 100px 200px 100px;        /* Fixed widths */
    grid-template-columns: 1fr 2fr 1fr;              /* Fractions */
    grid-template-columns: repeat(3, 1fr);           /* 3 equal columns */
    grid-template-columns: minmax(100px, 1fr) 2fr;   /* Min and max width */
    grid-template-columns: repeat(auto-fit, minmax(200px, 1fr)); /* Responsive */
    
    /* Defining Rows */
    grid-template-rows: 100px 200px;                  /* Fixed heights */
    grid-template-rows: 1fr 2fr;                       /* Flexible heights */
    
    /* Gap */
    gap: 20px;                  /* Both row and column gap */
    row-gap: 10px;
    column-gap: 15px;
    
    /* Aligning Grid Tracks */
    justify-content: start | end | center | stretch | space-around | space-between | space-evenly;
    align-content: start | end | center | stretch | space-around | space-between | space-evenly;
    
    /* Aligning Items Inside Cells */
    justify-items: start | end | center | stretch;
    align-items: start | end | center | stretch;
    
    /* Auto-generated Rows/Columns */
    grid-auto-rows: minmax(100px, auto);
    grid-auto-columns: minmax(50px, auto);
    grid-auto-flow: row | column | dense;
}
```
**Grid Item Properties:**
```css

.grid-item {
    /* Positioning by Lines */
    grid-column-start: 1;
    grid-column-end: 3;        /* Spans from line 1 to 3 */
    grid-row-start: 1;
    grid-row-end: 3;
    
    /* Shorthand */
    grid-column: 1 / 3;        /* Start / End */
    grid-row: 1 / 3;
    
    /* Spanning */
    grid-column: 1 / span 2;   /* Start at 1, span 2 columns */
    grid-row: span 2;          /* Span 2 rows from where placed */
    
    /* Naming Areas */
    grid-area: header;         /* Must match template areas */
    
    /* Individual Alignment */
    justify-self: start | end | center | stretch;
    align-self: start | end | center | stretch;
}
```
**Grid Template Areas:**
```css

.layout {
    display: grid;
    grid-template-columns: 200px 1fr 200px;
    grid-template-rows: auto 1fr auto;
    grid-template-areas: 
        "header header header"
        "nav    main   aside"
        "footer footer footer";
}

.header { grid-area: header; }
.nav { grid-area: nav; }
.main { grid-area: main; }
.aside { grid-area: aside; }
.footer { grid-area: footer; }
```

**Advanced Grid Patterns:**
```css

/* Responsive Gallery */
.gallery {
    display: grid;
    grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
    gap: 20px;
}

/* Masonry-like Layout */
.masonry {
    display: grid;
    grid-template-columns: repeat(4, 1fr);
    grid-auto-rows: 100px;
    gap: 10px;
}

.item-wide {
    grid-column: span 2;
}

.item-tall {
    grid-row: span 2;
}

/* Complex Dashboard */
.dashboard {
    display: grid;
    grid-template-columns: [sidebar] 200px [main] 1fr [aside] 300px;
    grid-template-rows: [header] auto [content] 1fr [footer] auto;
    gap: 20px;
}
```
## 9. Responsive Design & Media Queries
**Media Query Types:**
```css

/* Screen Size Queries */
@media (max-width: 768px) { ... }        /* Mobile */
@media (min-width: 769px) and (max-width: 1024px) { ... } /* Tablet */
@media (min-width: 1025px) { ... }       /* Desktop */

/* Orientation */
@media (orientation: portrait) { ... }
@media (orientation: landscape) { ... }

/* Resolution */
@media (min-resolution: 2dppx) { ... }   /* Retina displays */

/* Dark Mode */
@media (prefers-color-scheme: dark) { ... }

/* Reduced Motion */
@media (prefers-reduced-motion: reduce) {
    * { animation-duration: 0.01ms !important; }
}

/* Print Styles */
@media print {
    .no-print { display: none; }
    body { font-size: 12pt; }
}

/* Hover Capability */
@media (hover: hover) {
    .button:hover { background: blue; }
}
```
**Mobile-First Approach:**
```css

/* Base styles for mobile */
.container {
    width: 100%;
    padding: 10px;
}

/* Tablet */
@media (min-width: 768px) {
    .container {
        width: 750px;
        margin: 0 auto;
    }
}

/* Desktop */
@media (min-width: 1024px) {
    .container {
        width: 980px;
    }
}

/* Large Desktop */
@media (min-width: 1200px) {
    .container {
        width: 1170px;
    }
}
```
## 10. Transitions & Animations
**Transitions:**
```css

.button {
    background: blue;
    color: white;
    
    /* Property duration timing-function delay */
    transition: background-color 0.3s ease 0s;
    
    /* Multiple properties */
    transition: background-color 0.3s, transform 0.5s;
    
    /* All properties */
    transition: all 0.3s ease;
    
    /* Timing Functions */
    transition-timing-function: ease | linear | ease-in | ease-out | ease-in-out;
    transition-timing-function: cubic-bezier(0.1, 0.7, 1.0, 0.1); /* Custom */
    transition-timing-function: steps(4, end); /* Step animation */
}

.button:hover {
    background: darkblue;
    transform: scale(1.1);
}
```
**Keyframe Animations:**
```css

/* Define Animation */
@keyframes slideIn {
    0% {
        transform: translateX(-100%);
        opacity: 0;
    }
    50% {
        transform: translateX(10%);
    }
    100% {
        transform: translateX(0);
        opacity: 1;
    }
}

@keyframes pulse {
    from {
        transform: scale(1);
    }
    to {
        transform: scale(1.1);
    }
}

@keyframes complex {
    0%, 100% { 
        transform: rotate(0deg); 
        background: red;
    }
    33% { 
        transform: rotate(120deg); 
        background: blue;
    }
    66% { 
        transform: rotate(240deg); 
        background: green;
    }
}

/* Apply Animation */
.element {
    animation-name: slideIn;
    animation-duration: 2s;
    animation-timing-function: ease-out;
    animation-delay: 0.5s;
    animation-iteration-count: infinite;  /* or number */
    animation-direction: alternate;        /* normal, reverse, alternate */
    animation-fill-mode: forwards;         /* Keep final state */
    animation-play-state: running;         /* or paused */
    
    /* Shorthand */
    animation: slideIn 2s ease-out 0.5s infinite alternate forwards;
}

/* Animation with steps */
@keyframes typewriter {
    from { width: 0; }
    to { width: 100%; }
}

.typing {
    animation: typewriter 3s steps(30) 1s 1 normal both;
}
```
## 11. Advanced CSS Features
**Custom Properties (CSS Variables):**
```css

:root {
    --primary-color: #3498db;
    --secondary-color: #2ecc71;
    --spacing-unit: 8px;
    --border-radius: 4px;
    --font-stack: -apple-system, BlinkMacSystemFont, 'Segoe UI', sans-serif;
}

.element {
    color: var(--primary-color);
    padding: calc(var(--spacing-unit) * 2);
    border-radius: var(--border-radius);
    font-family: var(--font-stack);
}

/* Dynamic theming */
.dark-theme {
    --primary-color: #9b59b6;
    --background: #2c3e50;
}

/* Fallback values */
.unsupported {
    color: var(--undefined-color, #ff0000);  /* Falls back to red */
}
```
**CSS Functions:**
```css

.element {
    /* Calculations */
    width: calc(100% - 80px);
    height: calc(100vh - 60px);
    font-size: clamp(1rem, 5vw, 2rem);  /* Min, preferred, max */
    
    /* Mathematical */
    width: min(50%, 500px);              /* Smaller value */
    height: max(300px, 50vh);            /* Larger value */
    
    /* Color Functions */
    background: color-mix(in srgb, red 50%, blue);
    color: color-contrast(var(--bg) vs white, black);
    
    /* Grid Functions */
    grid-template-columns: repeat(3, minmax(100px, 1fr));
    grid-template-rows: fit-content(200px) auto;
    
    /* Filter Functions */
    filter: blur(5px);
    filter: brightness(1.2);
    filter: contrast(150%);
    filter: drop-shadow(5px 5px 5px gray);
    filter: grayscale(50%);
    filter: hue-rotate(90deg);
    filter: invert(100%);
    filter: opacity(50%);
    filter: saturate(200%);
    filter: sepia(80%);
    
    /* Multiple filters */
    filter: contrast(150%) brightness(1.2) drop-shadow(5px 5px 5px gray);
}
```

**Transformations:**
```css

.element {
    /* 2D Transforms */
    transform: translate(50px, 100px);
    transform: translateX(50px);
    transform: translateY(100px);
    transform: rotate(45deg);
    transform: scale(1.5);
    transform: scaleX(2);
    transform: scaleY(0.5);
    transform: skew(10deg, 20deg);
    transform: skewX(15deg);
    transform: skewY(10deg);
    
    /* 3D Transforms */
    transform: rotateX(45deg);
    transform: rotateY(30deg);
    transform: rotateZ(90deg);
    transform: translate3d(10px, 20px, 30px);
    transform: scale3d(1.5, 1.5, 2);
    
    /* Multiple Transforms */
    transform: translateX(50px) rotate(45deg) scale(1.5);
    
    /* Transform Origin */
    transform-origin: top left;
    transform-origin: 50% 50%;  /* Default */
    transform-origin: 0 0;
    
    /* 3D Perspective */
    perspective: 1000px;
    transform-style: preserve-3d;
    backface-visibility: hidden;
}
```
## 12. Best Practices & Performance
**CSS Methodology (BEM):**
```css

/* Block - standalone component */
.card { }

/* Element - part of block */
.card__title { }
.card__image { }
.card__button { }

/* Modifier - variation */
.card--featured { }
.card__button--primary { }
.card__button--large { }
```
**Performance Tips:**
```css

/* Use specific selectors instead of universal */
/* Bad */
* { box-sizing: border-box; }

/* Good */
html { box-sizing: border-box; }

/* Use will-change for animations */
.animated-element {
    will-change: transform, opacity;
}

/* Use contain for isolated components */
.widget {
    contain: layout style paint;
}

/* Optimize rendering */
.repaint-optimization {
    transform: translateZ(0);  /* Forces GPU acceleration */
    backface-visibility: hidden;
}
```
**Common Reset / Normalize:**
```css

/* Modern CSS Reset */
*,
*::before,
*::after {
    box-sizing: border-box;
    margin: 0;
    padding: 0;
}

/* Remove default styles */
ul, ol { list-style: none; }
a { text-decoration: none; color: inherit; }
img { max-width: 100%; display: block; }

/* Set core body defaults */
body {
    min-height: 100vh;
    line-height: 1.5;
    -webkit-font-smoothing: antialiased;
    -moz-osx-font-smoothing: grayscale;
}

/* Improve media defaults */
video, canvas, svg {
    display: block;
    max-width: 100%;
}
```