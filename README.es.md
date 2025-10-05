# 📝 Hoja Chuleta de CSS
Una guía rápida de referencia con la sintaxis esencial de CSS, selectores, propiedades y buenas prácticas.

---
<br>

## 🎨 Sintaxis Básica

```css
selector {
  propiedad: valor;
  propiedad: valor;
}
```

Ejemplo:
```css
h1 {
  color: blue;
  font-size: 24px;
}
```
<br>

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
| `[attribute]` | `[type]` | Selecciona elementos con el atributo especificado |
| `[attribute=value]` | `[type="text"]` | Selecciona elementos con atributo igual al valor |
| `:hover` | `a:hover` | Selecciona enlaces cuando el ratón pasa por encima |
| `::before` | `p::before` | Inserta contenido antes del elemento seleccionado |
| `::after` | `p::after` | Inserta contenido después del elemento seleccionado |
<br>

## 🖌️ Propiedades de Texto y Fuentes
| PROPIEDAD | VALORES | DESCRIPCIÓN |
|------|------------|-----|
| `color` | `red`, `#ff0000`, `rgb(255,0,0)` | Color del texto |
| `font-size` | `16px`, `1.2em`, `100%` | Tamaño de la fuente |
| `font-family` | `"Arial"`, `sans-serif` | Tipo de fuente |
| `font-weight` | `normal`, `bold`, `700` | Grosor del texto |
| `text-align` | `left`, `center`, `right`, `justify` | Alineación horizontal |
| `line-height` | `1.5`, `24px` | Espacio entre líneas |
| `text-decoration` | `none`, `underline`, `line-through` | Decoración del texto |
| `text-transform` | `uppercase`, `lowercase`, `capitalize` | Transformación del texto |
| `letter-spacing` | `2px`, `0.1em` | Espacio entre caracteres | 
| `word-spacing` | `4px`, `0.2em` | Espacio entre palabras |
| `text-shadow` | `2px 2px 5px black` | Sombra del texto (x, y, difusión, color)
<br>

## 📦 Modelo de Caja (Box Model)
| PROPIEDAD | DESCRIPCIÓN |
|------|------------|
| `width` / `height`| Define el ancho/alto del contenido de un elemento |
| `max-width` / `max-height` | Ancho/alto máximo que puede tener un elemento |
| `min-width` / `min-height` | Ancho/alto mínimo que puede tener un elemento |
| `pading` | Espacio inferior (entre contenido y borde) |
| `padding-top`, `padding-right`, etc. | Espacio interior específico por lado |
| `border` | Borde alrededor del padding (ej. `1px solid black`) |
| `border-radius` | Redondeo de las esquinas del borde |
| `margin` | Espacio exterior (entre elementos) |
| `margin-top`, `margin-right`, etc. | Espacio exterior específico por lado |
| `box-sizing` | `content-box` (default) o `border-box` (incluye padding y border en width/height) |
<br>

## Notación Abreviada
| FORMATO | EJEMPLO | APLICACIÓN |
| --------| --------| -----------|
| 1 valor | `margin: 10px;` | Todos los lados |
| 2 valores | `margin: 10px 20px;` | vertical (arriba/abajo)<br>horizontal (izquierda/derecha) |
| 3 valores | `margin: 10px 20px 30px;` | arriba<br>horizontal<br>abajo |
| 4 valores | `margin: 10px 20px 30px 40px;` | arriba<br>derecha<br>abajo<br>izquierda |
<br>

## 🎬 Visualización y Diseño
| PROPIEDAD | VALORES COMUNES | DESCRIPCIÓN |
|------|------------|-----|
| `display` | `block`, `inline`, `inline-block`, `flex`, `grid`, `none` | Cómo se muestra un elemento |
| `visibility` | `visible`, `hidden` | Muestra u oculta (mantiene el espacio) |
| `opacity` | `0` a `1` | Transparencia del elemento (0=invisible, 1=opaco) |
| `position` |  `static`, `relative`, `absolute`, `fixed`, `sticky` | Método de posicionamiento |
| `top`, `right`, `bottom`, `left` | `10px`, `50%` | Desplazamiento desde el borde correspondiente |
| `z-index` | `1`, `100`, `-1` | Orden de apilamiento (mayor número = frente) |
| `overflow` | `visible`, `hidden`, `scroll`, `auto` | Cómo manejar el contenido que sobrepasa |
| `float` | `left`, `right`, `none` | Hace flotar un elemento (no recomendado para layout) |
<br>

## 🔄 Flexbox (Contenedor Padre)
| PROPIEDAD | VALORES COMUNES | DESCRIPCIÓN |
|------|------------| ----- |
| `display: flex` | - |Activa Flexbox |
| `flex-direction` | `row`, `column`, `row-reverse`, `column-reverse` | Dirección del eje principal |
| `justify-content` | `flex-start`, `center`, `space-between`, `space-around`, `space-evenly` | Alineación en el eje principal | 
| `align-items` | `stretch`, `center`, `flex-start`, `flex-end`, `baseline` | Alineación en el eje transversal |
| `align-content` | `stretch`, `center`, `flex-start`, `flex-end`, `space-between` | Alineación de múltiples líneas |
| `flex-wrap` | `nowrap`, `wrap`, `wrap-reverse` | Control de desbordamiento de items |
| `gap` | `10px`, `1rem` | Espacio entre elementos flex |
<br>

## Flexbox (Elementos Hijos)
| PROPIEDAD | DESCRIPCIÓN |
|------|------------|
| `flex` | Abreviatura: `flex-growflex-shrinkflex-basis` (ej. `1 0 auto`) |
| `flex-grow` | Factor de crecimiento (`0` = no crece, `1+` = crece proporcionalmente) |
| `flex-shrink` | Factor de reducción (`0` = no se reduce, `1+` = se reduce) |
| `flex-basis` | Tamaño base antes de distribución (`auto`, `0`, `200px`) |
| `align-self` | Alineación individual que sobrescribe `align-items` |
| `order` | Cambia orden de visualización (`0` por defecto, acepta negativos) |
<br>

## 🔲 Grid (Contenedor Padre)
| PROPIEDAD | VALORES/EJEMPLOS | DESCRIPCIÓN |
|------|------------|-------|
| `display:grid` | - | Activa CSS Grid |
| `grid-template-columns` | `100px 100px`, `1fr 2fr`, `repeat(3, 1fr)` | Define columnas de la cuadrícula |
| `grid-template-rows` | `auto 100px`, `repeat(3, 100px)` | Define filas de la cuadrícula |
| `grid-template-areas` | `"header header" "sidebar main"` | Define áreas por nombre |
| `gap` o `grid-gap` | ``, `` | Espacio entre filas y columnas |
| `column-gap` o `row-gap` | `10px`, `1rem` | Espacio entre columnas o filas |
| `justify-items` | `start`, `center`, `end`, `stretch` | Alineación horizontal de los elementos |
| `align-items` | `start`, `center`, `end`, `stretch` | Alineación vertical de los elementos |
| `justify-content` | `start`, `center`, `end`, `space-between` | Alineación horizontal de toda la cuadrícula |
| `align-content` | `start`, `center`, `end`, `space-between` | Alineación vertical de toda la cuadrícula |
<br>

## Grid (Elementos Hijos)
| PROPIEDAD | EJEMPLOS | DESCRIPCIÓN |
|------|------------|-------|
| `grid-column` | `1 / 3`, `1 / span 2` | Ubicación en columnas (inicio / fin) |
| `grid-row` | `1 / 3`, `1 / span 2` | Ubicación en filas (inicio / fin) |
| `grid-area` | `header`, `2 / 1 / 3 / 3` | Área definida o atajado para fila-inicio/columna-inicio/fila-fin/columna-fin |
| `justify-self` | `start`, `center`, `end`, `stretch` | Alineación horizontal individual |
| `align-self` | `start`, `center`, `end`, `stretch` | Alineación vertical individual |
<br>

## 📏 Unidades
| UNIDAD | DESCRIPCIÓN |
|------|------------|
| `px` | Píxeles (absoluta) |
| `%` | Porcentaje del contenedor padre |
| `em` | Relativa al tamaño de fuente del elemento |
| `rem` | Relativa al tamaño de fuente de la raíz (`<html>`) |
| `vh` / `vw` | 1% de la altura/anchura del viewport |
| `vmin` / `vmax` | 1% del valor más pequeño/grande del viewport (ancho o alto) |
| `ch` | Anchura del carácter "0" de la fuente actual |
| `ex` | Altura de la letra "x" de la fuente actual |
| `fr` | Fracción del espacio disponible (solo en Grid) |
<br>

## 🌈 Colores
| FORMATO | EJEMPLO | DESCRIPCIÓN |
|------|------------| --------| 
| Nombre | `red`, `blue`, `transparent` | Nombres predefinidos (140 en CSS) |
| Hexadecimal | `#ff0000`, `#f00` (forma corta) | Valores RGB en base 16 |
| RGB | `rgb(255,0,0)` | Valores Red, Green, Blue (0-255) |
| RGBA | `rgba(255,0,0,0.5)` | RGB con canal Alpha (opacidad 0-1) |
| HSL | `hsl(0,100%,50%)` | Hue (0-360), Saturation, Lightness |
| HSLA | `hsl(0,100%,50%,0.5)` | HSL con canal Alpha (opacidad 0-1) |
| currentColor | `border: 1px solid currentColor;` | Utiliza el valor de la propiedad color actual |
<br>

## 🎭 Transformaciones y Animaciones
| PROPIEDAD | EJEMPLO | DESCRIPCIÓN |
|------|------------|-------|
| `transform` | `rotate(45deg)`, `scale(1.5)` | Aplica transformaciones visuales |
| `transform-origin` | `center`, `top left`, `50% 50%` | Define punto de origen de transformación |
| `transition` | `all 0.3s ease` | Transición suave entre estados |
| `animation` | `fadeIn 2s ease-in-out` | Animación usando keyframes |
<br>

## Funciones de Transformación
| FUNCIÓN | EJEMPLO | DESCRIPCIÓN |
|------|------------|-------|
| `translate(x,y)` | `translate(20px, 30px)` | Mueve el elemento horizontal y verticalmente |
| `translateX(x)`, `translateY(y)` | `translateY(-10px)` | Mueve el elemento en un solo eje |
| `scale(x,y)` | `scale(1.5)`, `scale(1.5, 0.5)` | Cambia el tamaño del elemento |
| `rotate(angle)` | `rotate(45deg)` | Rota el elemento |
| `skew(x-angle,y-angle)` | `skew(10deg, 20deg)` | Inclina el elemento |
<br>

## Transiciones
Notación completa: `transition: property duration timing-function delay;
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

## Animaciones
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

## 📱 Diseño Responsivo
Media queries para adaptar el diseño a diferentes tamaños de pantalla:
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

Puntos de ruptura comunes:
| DISPOSITIVO | ANCHO |
| ----- | ----- |
| Móviles pequeños | `< 576px` |
| Móviles grandes | `576px - 767px` |
| Tablets | `768px - 991px` |
| Escritorios pequeños | `992px - 1199px` |
| Escritorios grandes | `≥ 1200px` |

Otras propiedades responsivas:
| PROPIEDAD | DESCRIPCIÓN |
| ----- | ----- |
| `max-width: 100%` | Imágenes y elementos responsivos |
| `object-fit` | Controla cómo se redimensiona una imagen (`cover`, `contain`) |
| `flex-wrap: wrap` | Permite que los elementos flex se ajusten a nuevas líneas |
| `column-count` | Divide el contenido en columnas |
<br>

## 🛠️ Funciones y Variables
Variables CSS (Custom Properties)
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

Funciones CSS Comunes
| PROPIEDAD | EJEMPLO | DESCRIPCIÓN |
|------|------------|-------|
| `calc()` | `width: calc(100% - 20px);` | Realiza cálculos con diferentes unidades |
| `clamp()` | `font-size: clamp(1rem, 5vw, 2rem);` | Valor entre mínimo y máximo con preferencia |
| `min()` | `width: min(300px, 100%);` | Elige el valor más pequeño |
| `max()` | `width: max(50%, 300px);` | Elige el valor más grande |
| `var()` | `color: var(--main-color, black);` | Usa una variable CSS con valor alternativo |
<br>

## ✅ Buenas Prácticas
- Usa clases en lugar de IDs para estilos (los IDs son para JavaScript y anclajes).
- Prefiere unidades relativas (`rem`, `em`, `%`) para mejor accesibilidad y escalabilidad.
- Organiza el CSS de forma modular (por componentes o secciones).
- Utiliza una nomenclatura consistente para clases (BEM, OOCSS, etc.).
- Aprovecha Flexbox y Grid para diseños modernos - evita usar `float` para maquetación.
- Adopta un enfoque mobile-first para diseño responsivo.
- Usa CSS Custom Properties (variables) para valores reutilizables.
- Implementa media queries para asegurar compatibilidad con diferentes dispositivos. 
- Minimiza y combina archivos CSS en producción para mejor rendimiento.
- Utiliza comentarios para explicar secciones complejas. 
- Evita la especificidad excesiva de selectores.
- Considera usar un preprocesador como SASS o LESS para proyectos grandes.
<br>

## 📚 Glosario
- **BEM**: metodología de nomenclatura de clases (Block, Element, Modifier).
- **Box Model**: modelo que describe cómo se renderiza cada elemento como una caja rectangular.
- **Cascada**: mecanismo que determina el orden y la prioridad de aplicación de estilos.
- **Declaración**: par propiedad-valor (ej. `color: red;`)
- **Especificidad**: sistema que determina qué estilos se aplican cuando hay conflictos.
- **Fallback**: valor alternativo que se usa cuando el navegador no soporta una propiedad.
- **Flexbox**: modelo de diseño unidimensional para distribuir elementos en filas o columnas.
- **Grid**: sistema de diseño bidimensional para crear layouts complejos.
- **Herencia**: proceso por el que los elementos hijos reciben propiedades de elementos padres.
- **Media Query**: condición que permite aplicar estilos según características del dispositivo.
- **Normalize/Reset**: técnicas para estandarizar estilos predeterminados entre navegadores.
- **Propiedad**: característica de un elemento que se puede modificar con CSS.
- **Pseudoclase**: selector que especifica un estado especial del elemento (ej.`:hover`).
- **Pseudoelemento**: selector que estiliza una parte específica de un elemento (ej. `::before`).
- **Regla CSS**: selector seguido de un bloque de declaraciones.
- **Responsive Design**: enfoque que permite adaptar sitios web a diferentes tamaños de pantalla.
- **Selector**: patrón que identifica qué elementos HTML serán estilizados.
- **Valor**: configuración específica asignada a una propiedad.
- **Viewport**: área visible del navegador donde se muestra el contenido.
- **Z-index**: propiedad que controla la superposición vertical de los elementos.
<br>

> 💡 **Consejo**: para documentación completa, visita [MDN Web Docs - CSS](https://developer.mozilla.org/es/docs/Web/CSS).
