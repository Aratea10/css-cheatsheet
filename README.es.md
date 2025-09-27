# 📝 Hoja Chuleta de CSS

Una guía rápida de referencia con la sintaxis esencial de CSS, selectores, propiedades y buenas prácticas.

---

## 🎨 Sintaxis Básica

```css
selector {
  propiedad: valor;
  propiedad: valor;
}
```

Ejemplo:
```
h1 {
  color: blue;
  font-size: 24px;
}
```

## 🔍 Selectores
| SELECTOR | EJEMPLO | DESCRIPCIÓN |
|------|------------|-----|
| `*` | `*` | Selector universal (selecciona todos los elementos) |
| `element` | `p` | Selecciona todos los elementos `<p>` |
| `.class` | `.intro` | Selecciona todos los elementos con `class="intro"`|
| `#id` | `#header` | Selecciona el elemento con `id="header"` |
| `element, element` | `div, p` | Selecciona todos los `<div>` y `<p>` |
| `element element` | `div p` | Selecciona todos los `<p>` dentro de `<div>` |
| `element > element` | `div > p` |  Selecciona `<p>` que son hijos directos de `<div>` |
| `element + element` | `h1 + p` | Selecciona el primer `<p>` inmediatamente después de un `<h1>`|
| `element ~ element` | `h1 ~ p` | Selecciona todos los `<p>` hermanos posteriores a un `<h1>`|

## 🖌️ Propiedades Comunes
Texto y Fuentes
| PROPIEDAD | VALORES | DESCRIPCIÓN |
|------|------------|-----|
| `color` | `red`, `#ff0000`, `rgb(255,0,0)` | Color de texto |
| `font-size` | `16px`, `1.2em`, `100%` | Tamaño de la fuente |
| `font-family` | `"Arial"`, `sans-serif` | Tipo de fuente |
| `font-weight` | `normal`, `bold`, `700` | Grosor del texto |
| `text-align` | `left`, `center`, `right`, `justify` | Alineación horizontal |
| `line-height` | `1.5`, `24px` | Espacio entre líneas |

## Modelo de Caja (Box Model)
| PROPIEDAD | DESCRIPCIÓN |
|------|------------|
| `width` / `height`| Define el tamaño de un elemento |
| `pading` | Espacio inferior (entre contenido y borde) |
| `border` | Borde alrededor del padding (ej. `1px solid black`) |
| `margin` | Espacio exterior (entre elementos) |

## Visualización y Diseño
| PROPIEDAD | VALORES COMUNES | DESCRIPCIÓN |
|------|------------|-----|
| `display` | `block`, `inline`, `inline-block`, `flex`, `grid`, `none` | Cómo se muestra un elemento |
| `visibility` | `visible`, `hidden` | Muestra u oculta (mantiene el espacio) |
| `position` |  `static`, `relative`, `absolute`, `fixed`, `sticky` | Método de posicionamiento |
`top`, `right`, `bottom`, `left` | Usados con `position` para desplazar el elemento |

## Flexbox (Contenedor Padre)
| PROPIEDAD | VALORES COMUNES |
|------|------------|
| `display: flex` | Activa Flexbox |
| `flex-direction` | `row`, `column`, `row-reverse`, `column-reverse` |
| `justify-content` | `flex-start`, `center`, `space-between`, `space-around` | 
| `align-items` | `stretch`, `center`, `flex-start`, `flex-end` |
| `flex-wrap` | `nowrap`, `wrap` |

## Grid (Contenedor Padre)
| PROPIEDAD | DESCRIPCIÓN |
|------|------------|
| `display:grid` | Activa CSS Grid |
| `grid-template-columns` | `1fr 1fr 1fr`, `repeat(3, 100px)` | 
| `grid-template-rows` | `auto 100px` | 
| `gap` | `10px`, `1rem` (espacio entre elementos de la cuadrícula) |

## 📏 Unidades
| UNIDAD | DESCRIPCIÓN |
|------|------------|
| `px` | Píxeles (absoluta) |
| `%` | Porcentaje del contenedor padre |
| `em` | Relativa al tamaño de fuente del elemento |
| `rem` | Relativa al tamaño de fuente de la raíz (`<html>`) |
| `vh` / `vw` | 1% de la altura/anchura del viewport |

## 🌈 Colores
| FORMATO | EJEMPLO |
|------|------------|
| Nombre | `red`, `blue`, `transparent` |
| Hexadecimal | `#ff0000`, `#f00` |
| RGB | `rgb(255,0,0)` |
| RGBA | `rgba(255,0,0,0.5)` |
| HSL | `hsl(0,100%,50%)` |
| HSLA | `hsl(0,100%,50%,0.5)` |

## 📱 Diseño Responsivo
````
/* Mobile-first media query */
@media (min-width: 768px) {
  .container {
    width: 750px;
  }
}
````

Puntos de quiebre comunes:
- Móvil: ```< 768px```
- Tablet: ```768px – 1023px```
- Escritorio: ```≥ 1024px```

## ✅ Buenas Prácticas
- Usa clases en lugar de IDs para estilos.
- Prefiere unidades relativas (```rem```, ```em```, ```%```) para mejor escalabilidad.
- Mantén el CSS modular y organizado (por componente o sección).
- Usa nombres de clase descriptivos (ej. ```.btn-primary```, no ```.red-button```).
- Aprovecha Flexbox y Grid para diseños modernos - evita usar ```float```para maquetación.
- Minimiza el CSS en producción.

> 💡 **Consejo**: Para documentación completa, visita [MDN Web Docs - CSS](https://developer.mozilla.org/es/docs/Web/CSS).