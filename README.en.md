# 📝 CSS Cheat Sheet
A quick reference guide with essential CSS syntax, selectors, properties, and best practices.

---
<br>

## 🎨 Sintaxis Básica

```css
selector {
  property: value;
  property: value;
}
```

Example:
```css
h1 {
  color: blue;
  font-size: 24px;
}
```
<br>

## 🔍 Selectors
| SELECTOR | EXAMPLE | DESCRIPTION |
|------|------------|-----|
| `*` | `*` | Universal selector (selects all elements) |
| `element` | `p` | Selects all `<p>` elements |
| `.class` | `.intro` | Selects all elements with `class="intro"`|
| `#id` | `#header` | Selects the element with `id="header"` |
| `element, element` | `div, p` | Selects all `<div>` and `<p>` |
| `element element` | `div p` | Selects all `<p>` inside `<div>` |
| `element > element` | `div > p` |  Selects `<p>` that are direct children of `<div>` |
| `element + element` | `h1 + p` | Selects the first `<p>` immediately after an `<h1>`|
| `element ~ element` | `h1 ~ p` | Selects all `<p>` siblings after an `<h1>`|
| `[attribute]` | `[type]` | Selects elements with the specified attribute |
| `[attribute=value]` | `[type="text"]` | Selects elements with attribute equal to value |
| `:hover` | `a:hover` | Selects links when mouse hovers over them |
| `::before` | `p::before` | Inserts content before the selected element |
| `::after` | `p::after` | Inserts content after the selected element |
<br>

## 🖌️ Text and Font Properties
| PROPERTY | VALUES | DESCRIPTION |
|------|------------|-----|
| `color` | `red`, `#ff0000`, `rgb(255,0,0)` | Text color |
| `font-size` | `16px`, `1.2em`, `100%` | Font size |
| `font-family` | `"Arial"`, `sans-serif` | Font type |
| `font-weight` | `normal`, `bold`, `700` | Text thickness |
| `text-align` | `left`, `center`, `right`, `justify` | Horizontal alignment |
| `line-height` | `1.5`, `24px` | Line spacing |
| `text-decoration` | `none`, `underline`, `line-through` | Text decoration |
| `text-transform` | `uppercase`, `lowercase`, `capitalize` | Text transformation |
| `letter-spacing` | `2px`, `0.1em` | Character spacing | 
| `word-spacing` | `4px`, `0.2em` | Word spacing |
| `text-shadow` | `2px 2px 5px black` | Text shadow (x, y, blur, color))
<br>

## 📦 Box Model
| PROPERTY | DESCRIPTION |
|------|------------|
| `width` / `height`| Defines the width/height of an element's content |
| `max-width` / `max-height` | Maximum width/height an element can have |
| `min-width` / `min-height` | Minimum width/height an element can have |
| `pading` | Interior space (between content and border) |
| `padding-top`, `padding-right`, etc. | Specific interior space per side |
| `border` | Border around the padding (e.g. `1px solid black`) |
| `border-radius` | Rounding of border corners |
| `margin` | Exterior space (between elements) |
| `margin-top`, `margin-right`, etc. | Specific exterior space per side |
| `box-sizing` | `content-box` (default) or `border-box` (includes padding and border in width/height) |
<br>

## Shorthand Notation
| FORMAT | EXAMPLE | APPLICATION |
| --------| --------| -----------|
| 1 value | `margin: 10px;` | All sides |
| 2 values | `margin: 10px 20px;` | vertical (top/bottom)<br>horizontal (left/right) |
| 3 values | `margin: 10px 20px 30px;` | top<br>horizontal<br>bottom |
| 4 values | `margin: 10px 20px 30px 40px;` | top<br>right<br>bottom<br>left (clockwise) |
<br>

## 🎬 Display and Layout
| PROPERTY | COMMON VALUES | DESCRIPTION |
|------|------------|-----|
| `display` | `block`, `inline`, `inline-block`, `flex`, `grid`, `none` | How an element is displayed |
| `visibility` | `visible`, `hidden` | Shows or hides (maintains the space) |
| `opacity` | `0` to `1` | Element transparency (0=invisible, 1=opaque) |
| `position` |  `static`, `relative`, `absolute`, `fixed`, `sticky` | Positioning method |
| `top`, `right`, `bottom`, `left` | `10px`, `50%` | Offset from the corresponding edge |
| `z-index` | `1`, `100`, `-1` | Stacking order (higher number = front) |
| `overflow` | `visible`, `hidden`, `scroll`, `auto` | How to handle content that overflows |
| `float` | `left`, `right`, `none` | Floats an element (not recommended for layout) |
<br>

## 🔄 Flexbox (Parent Container)
| PROPERTY | COMMON VALUES | DESCRIPTION |
|------|------------| ----- |
| `display: flex` | - | Activates Flexbox |
| `flex-direction` | `row`, `column`, `row-reverse`, `column-reverse` | Direction of the main axis |
| `justify-content` | `flex-start`, `center`, `space-between`, `space-around`, `space-evenly` | Alignment along the main axis | 
| `align-items` | `stretch`, `center`, `flex-start`, `flex-end`, `baseline` | Alignment along the cross axis |
| `align-content` | `stretch`, `center`, `flex-start`, `flex-end`, `space-between` | Alignment of multiple lines |
| `flex-wrap` | `nowrap`, `wrap`, `wrap-reverse` | Control of item overflow |
| `gap` | `10px`, `1rem` | Space between flex items |
<br>

## Flexbox (Child Elements)
| PROPERTY | DESCRIPTION |
|------|------------|
| `flex` | Shorthand: `flex-growflex-shrinkflex-basis` (eg. `1 0 auto`) |
| `flex-grow` | Growth factor (`0` = doesn't grow, `1+` = grows proportionally) |
| `flex-shrink` | Shrink factor (`0` = doesn't shrink, `1+` = shrinks) |
| `flex-basis` | Base size before distribution (`auto`, `0`, `200px`) |
| `align-self` | Individual alignment that overrides `align-items` |
| `order` | Changes display order (`0` by default, accepts negative values) |
<br>

## 🔲 Grid (Parent Container)
| PROPERTY | VALUES/EXAMPLES | DESCRIPTION |
|------|------------|-------|
| `display:grid` | - | Activates CSS Grid |
| `grid-template-columns` | `100px 100px`, `1fr 2fr`, `repeat(3, 1fr)` | Defines grid columns |
| `grid-template-rows` | `auto 100px`, `repeat(3, 100px)` | Defines grid rows |
| `grid-template-areas` | `"header header" "sidebar main"` | Defines named areas |
| `gap` or `grid-gap` | ``, `` | Space between rows and columns |
| `column-gap` or `row-gap` | `10px`, `1rem` | Space between columns or rows |
| `justify-items` | `start`, `center`, `end`, `stretch` | Horizontal alignment of elements |
| `align-items` | `start`, `center`, `end`, `stretch` | Vertical alignment of elements |
| `justify-content` | `start`, `center`, `end`, `space-between` | Horizontal alignment of the entire grid |
| `align-content` | `start`, `center`, `end`, `space-between` | Vertical alignment of the entire grid |
<br>

## Grid (Child Elements)
| PROPERTY | EXAMPLES | DESCRIPTION |
|------|------------|-------|
| `grid-column` | `1 / 3`, `1 / span 2` | Column placement (start / end) |
| `grid-row` | `1 / 3`, `1 / span 2` | Row placement (start / end) |
| `grid-area` | `header`, `2 / 1 / 3 / 3` | Defined area or shorthand for row-start/column-start/row-end/column-end |
| `justify-self` | `start`, `center`, `end`, `stretch` | Individual horizontal alignment |
| `align-self` | `start`, `center`, `end`, `stretch` | Individual vertical alignment |
<br>

## 📏 Unit
| UNIT | DESCRIPTION |
|------|------------|
| `px` | Pixels (absolute) |
| `%` | Percentage of parent container |
| `em` | Relative to font size of the element |
| `rem` | Relative to root font size (`<html>`) |
| `vh` / `vw` | 1% of viewport height/width |
| `vmin` / `vmax` | 1% of the smallest/largest viewport value (width or height) |
| `ch` | Width of the "0" character in the current font |
| `ex` | Height of the letter "x" in the current font |
| `fr` | Fraction of available space (Grid only) |
<br>

## 🌈 Colors
| FORMAT | EXAMPLE | DESCRIPTION |
|------|------------| --------| 
| Name | `red`, `blue`, `transparent` | Predefined names (140 in CSS) |
| Hexadecimal | `#ff0000`, `#f00` (shorthand) | RGB values in base 16 |
| RGB | `rgb(255,0,0)` | RGB with Alpha channel (opacity 0-1) |
| RGBA | `rgba(255,0,0,0.5)` | RGB con canal Alpha (opacidad 0-1) |
| HSL | `hsl(0,100%,50%)` | Hue (0-360), Saturation, Lightness |
| HSLA | `hsl(0,100%,50%,0.5)` | HSL with Alpha channel (opacity 0-1) |
| currentColor | `border: 1px solid currentColor;` | Uses the current color property value |
<br>

## 🎭 Transformations and Animations
| PROPERTY | EXAMPLE | DESCRIPTION |
|------|------------|-------|
| `transform` | `rotate(45deg)`, `scale(1.5)` | Applies visual transformations |
| `transform-origin` | `center`, `top left`, `50% 50%` | Defines transformation origin point |
| `transition` | `all 0.3s ease` | Smooth transition between states |
| `animation` | `fadeIn 2s ease-in-out` | Animation using keyframes |
<br>

## Transform Functions
| FUNCTION | EXAMPLE | DESCRIPTION |
|------|------------|-------|
| `translate(x,y)` | `translate(20px, 30px)` | Moves the element horizontally and vertically |
| `translateX(x)`, `translateY(y)` | `translateY(-10px)` | Moves the element on a single axis |
| `scale(x,y)` | `scale(1.5)`, `scale(1.5, 0.5)` | Changes the size of the element |
| `rotate(angle)` | `rotate(45deg)` | Rotates the element |
| `skew(x-angle,y-angle)` | `skew(10deg, 20deg)` | Skews the element |
<br>

## Transitions
Complete notation: `transition: property duration timing-function delay;
```css
.button {
  background-color: blue;
  transition: background-color 0.3s ease;
}
.button:hover {
  background-color: red;
}
```
<br>

## Animations
```css
@keyframes fadeIn {
  from { opacity: 0; }
  to { opacity: 1; }
}

.element {
  animation: fadeIn 1s ease-out;
  /* También podemos usar:
  animation-name: fadeIn;
  animation-duration: 1s;
  animation-timing-function: ease-out;
  animation-delay: 0s;
  animation-iteration-count: 1;
  animation-direction: normal;
  animation-fill-mode: forwards; */
}
```
<br>

## 📱 Responsive Design
Media queries to adapt the layout to different screen sizes:
```css
/* Mobile-first approach */
.container {
  width: 100%;
  padding: 15px;
}

/* Tablets y pantallas pequeñas */
@media (min-width: 768px) {
  .container {
    width: 750px;
    padding: 20px;
  }
}

/* Pantallas medianas */
@media (min-width: 992px) {
  .container {
    width: 970px;
  }
}

/* Pantallas grandes */
@media (min-width: 1200px) {
  .container {
    width: 1170px;
  }
}
```
<br>

Common Breakpoints:
| DEVICE | WIDTH |
| ----- | ----- |
| Small mobile | `< 576px` |
| Large mobile | `576px - 767px` |
| Tablets | `768px - 991px` |
| Small desktops | `992px - 1199px` |
| Large desktops | `≥ 1200px` |

### Other Responsive Properties
| PROPERTY | DESCRIPTION |
| ----- | ----- |
| `max-width: 100%` | Responsive images and elements |
| `object-fit` | Controls how an image is resized (`cover`, `contain`) |
| `flex-wrap: wrap` | Allows flex items to wrap to new lines |
| `column-count` | Divides content into columns |
<br>

## 🛠️ Functions and Variables
CSS Variables (Custom Properties)
```css
:root {
  --color-primary: #3498db;
  --spacing-unit: 8px;
  --font-main: 'Roboto', sans-serif;
}

.button {
  background-color: var(--color-primary);
  padding: calc(var(--spacing-unit) *2);
  font-family: var(--font-main);
}
```
<br>

Common CSS Functions
| FUNCTION | EXAMPLE | DESCRIPTION |
|------|------------|-------|
| `calc()` | `width: calc(100% - 20px);` | Performs calculations with different units |
| `clamp()` | `font-size: clamp(1rem, 5vw, 2rem);` | Value between minimum and maximum with preference |
| `min()` | `width: min(300px, 100%);` | Chooses the smallest value |
| `max()` | `width: max(50%, 300px);` | Chooses the largest value |
| `var()` | `color: var(--main-color, black);` | Uses a CSS variable with fallback value |
<br>

## ✅ Best Practices
- Use classes instead of IDs for styles (IDs are for JavaScript and anchors).
- Prefer relative units (`rem`, `em`, `%`) for better accessibility and scalability.
- Organize CSS in a modular way (by components or sections).
- Use a consistent naming convention for classes (BEM, OOCSS, etc.).
- Take advantage of Flexbox and Grid for modern layouts - avoid using `float` for layout.
- Adopt a mobile-first approach for responsive design.
- Use CSS Custom Properties (variables) for reusable values.
- Implement media queries to ensure compatibility with different devices. 
- Minimize and combine CSS files in production for better performance.
- Use comments to explain complex sections.
- Avoid excessive specificity in selectors.
- Consider using a preprocessor like SASS or LESS for large projects.
<br>

## 📚 Glossary
- **BEM**: class naming methodology (Block, Element, Modifier).
- **Box Model**: model that describes how each element is rendered as a rectangular box.
- **Cascade**: mechanism that determines the order and priority of style application.
- **CSS Rule**: selector followed by a block of declarations.
- **Declaration**: property-value pair (e.g. `color: red;`).
- **Fallback**: alternative value used when the browser doesn't support a property.
- **Flexbox**: one-dimensional layout model for distributing elements in rows or columns.
- **Grid**: two-dimensional layout system for creating complex layouts.
- **Inheritance**: process by which child elements receive properties from parent elements.
- **Media Query**: condition that allows applying styles based on device characteristics.
- **Normalize/Reset**: techniques to standardize default styles across browsers.
- **Property**: characteristic of an element that can be modified with CSS.
- **Pseudoclass**: selector that specifies a special state of the element (e.g.`:hover`).
- **Pseudoelement**: selector that styles a specific part of an element (e.g. `::before`).
- **Responsive Design**: enfoque que permite adaptar sitios web a diferentes tamaños de pantalla.
- **Selector**: patrón que identifica qué elementos HTML serán estilizados.
- **Specificity**: system that determines which styles are applied when there are conflicts.
- **Value**: specific configuration assigned to a property.
- **Viewport**: visible area of the browser where content is displayed.
- **Z-index**: property that controls the vertical stacking of elements.
<br>

> 💡 **Tip**: for complete and updated documentation, visit [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS).
