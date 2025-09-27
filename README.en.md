# 📝 CSS Cheatsheet

A quick reference guide to essential CSS syntax, selectors, properties, and best practices.

---

## 🎨 Basic Syntax

```css
selector {
  property: value;
  property: value;
}
```

Example:
```
h1 {
  color: blue;
  font-size: 24px;
}
```

## 🔍 Selectors
| SELECTOR | EXAMPLE | DESCRIPTION |
|------|------------|-----|
| `*` | `*` | Universal selector (selects all elements) |
| `element` | `p` | Selects all `<p>` elements |
| `.class` | `.intro` | Selects all elements with `class="intro"`|
| `#id` | `#header` | Selects the element with `id="header"` |
| `element, element` | `div, p` | Selects all `<div>`and `<>`elements |
| `element element` | `div p` | Selects all `<p>` inside `<div>` |
| `element > element` | `div > p` |  Selects `<p>` inside `<div>` |
| `element + element` | `h1 + p` | Selects the first `<p>` inmediately after an `<h1>`|
| `element ~ element` | `h1 ~ p` | Selects all siblings after an `<h1>`|

## 🖌️ Common Properties
| PROPERTY | VALUES | DESCRIPTION |
|------|------------|-----|
| `color` | `red`, `#ff0000`, `rgb(255,0,0)` | Text color |
| `font-size` | `16px`, `1.2em`, `100%` | Size of the font |
| `font-family` | `"Arial"`, `sans-serif`, `` | Font type |
| `font-weight` | `normal`, `bold`, `700` | Thickness of text |
| `text-align` | `left`, `center`, `right`, `justify` | Horizontal alignment |
| `line-height` | `1.5`, `24px` | Space between lines |

## Box Model
| PROPERTY | DESCRIPTION |
|------|------------|
| `width` / `height`| Sets the size of an element |
| `pading` | Sets the size of an element |
| `border` | Edge aroung padding (e.g., `1px solid black`) |
| `margin` | Space outside the border (between elements) |

## Display & Layout
| PROPERTY | COMMON VALUES | DESCRIPTION |
|------|------------|-----|
| `display` | `block`, `inline`, `inline-block`, `flex`, `grid`, `none` | How an element is displayed |
| `visibility` | `visible`, `hidden` | Shows/hides element (keeps space) |
| `position` |  `static`, `relative`, `absolute`, `fixed`, `sticky` | Positioning method |
`top`, `right`, `bottom`, `left` | Used with `position`to offset element |

## Flexbox (Parent)
| PROPERTY | COMMON VALUES |
|------|------------|
| `display: flex` | Enables flexbox |
| `flex-direction` | `row`, `column`, `row-reverse`, `column-reverse` |
| `justify-content` | `flex-start`, `center`, `space-between`, `space-around` | 
| `align-items` | `stretch`, `center`, `flex-start`, `flex-end` |
| `flex-wrap` | `nowrap`, `wrap` |

## Grid (Parent)
| PROPERTY | DESCRIPTION |
|------|------------|
| `display:grid` | Enables CSS Grid |
| `grid-template-columns` | `1fr 1fr 1fr`, `repeat(3, 100px)` | 
| `grid-template-rows` | `auto 100px` | 
| `gap` | `10px`, `1rem` (space between grid items) |

## 🎯 Units
| UNIT | DESCRIPTION |
|------|------------|
| `px` | Pixels (absolute) |
| `%` | Percentage of parent |
| `em` | Relative to font-size of the element |
| `rem` | Relative to font-size of the root (`<html>`) |
| `vh` / `vw` | 1% of viewport height/width |

## 🌈 Colors
| FORMAT | EXAMPLE |
|------|------------|
| Named | `red`, `blue`, `transparent` |
| Hex | `#ff0000`, `#f00` |
| RGB | `rgb(255,0,0)` |
| RGBA | `rgba(255,0,0,0.5)` |
| HSL | `hsl(0,100%,50%)` |
| HSLA | `hsl(0,100%,50%,0.5)` |

## 📱 Responsive Design
````
/* Mobile-first media query */
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
````

Common breakpoints:
- Mobile: ```< 768px```
- Tablet: ```768px – 1023px```
- Desktop: ```≥ 1024px```

## ✅ Best Practices
- Use classes instead of IDs for styling.
- Prefer relative units (```rem```, ```em```, ```%```) for scalability.
- Keep CSS modular and organized (e.g., by component or section).
- Use meaningful class names (e.g., ```.btn-primary```, not ```.red-button```).
- Leverage Flexbox and Grid for modern layouts-avoid floats for layout.
- Always minify CSS in production.

> 💡 **Tip**: For full documentation, visit [MDN Web Docs - CSS](https://developer.mozilla.org/en-US/docs/Web/CSS).