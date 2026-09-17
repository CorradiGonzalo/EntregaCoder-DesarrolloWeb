# Antares SRL — sitio web corporativo

Sitio institucional de **Antares SRL**, empresa cordobesa de pulvimetalurgia y
mecanizado de precisión en carburo de tungsteno, con más de 66 años de
trayectoria en herramental de corte y componentes para las industrias
petrolera, automotriz, agropecuaria, aeronáutica y maderera.

El sitio presenta la historia de la empresa, su catálogo técnico de
productos y servicios, la certificación de calidad ISO 9001:2015 y un canal
de contacto para consultas técnicas y cotizaciones.

**Demo en producción:** _agregar aquí el link de Vercel / Netlify una vez desplegado_

## Estructura del proyecto

```
├── index.html                  # Página de inicio
├── pages/
│   ├── sobrenosotros.html      # Historia y capacidad industrial
│   ├── productosyservicios.html# Catálogo técnico
│   ├── garantiadecalidad.html  # Certificación ISO 9001:2015
│   └── contacto.html           # Formulario y datos de contacto
├── scss/                       # Fuente Sass (variables, mixins, partials)
│   ├── abstracts/               # Variables, mixins y placeholders (%extend)
│   ├── base/                    # Reset, elementos base, animaciones
│   ├── layout/                  # Contenedor y footer
│   ├── components/              # Navbar, botones, modales, formularios
│   ├── pages/                   # Estilos específicos de cada página
│   └── main.scss                # Punto de entrada — solo @use
├── styles/
│   └── styles.css               # CSS compilado desde scss/main.scss
├── script/
│   └── script.js                # i18n, menú, modales, formulario, AOS
├── assets/
│   ├── img/                     # Imágenes (optimizadas, <1MB cada una)
│   └── certificados/             # Certificado ISO en PDF
└── README.md
```

## Tecnologías utilizadas

- **HTML5 semántico** (`header`, `nav`, `main`, `section`, `article`, `footer`)
- **Sass/SCSS** — variables, nesting, mixins con parámetros (`respond()`,
  `flex()`, `button-variant()`), `%placeholders` con `@extend` y partials,
  compilado a CSS plano en `styles/`
- **Bootstrap 5** — navbar responsiva con `navbar-toggler` / `collapse`
  (funciona en mobile), restyleada completamente desde SCSS para mantener
  la identidad visual de la marca
- **AOS (Animate On Scroll)** — animaciones al hacer scroll, combinadas con
  animaciones nativas en SCSS (`@keyframes`, `transition`)
- **JavaScript vanilla** — sistema de traducción ES/EN, menú, modales
  (certificado ISO, catálogo), validación y envío de formulario de contacto
- Tipografías Google Fonts (Barlow / Kanit)

## Diseño responsivo

El sitio es 100% responsivo (mobile, tablet, desktop) mediante media queries
propias (sin depender del grid de Bootstrap), sin scroll horizontal ni
compresión de elementos.

## SEO

Cada una de las 5 páginas tiene `<title>`, `<meta name="description">` y
`<meta name="keywords">` únicos y descriptivos, además de atributos `alt`
completos en todas las imágenes.

## Cómo correr el proyecto localmente

Es un sitio estático: alcanza con abrir `index.html` en el navegador, o
servirlo con cualquier servidor estático, por ejemplo:

```bash
npx serve .
```

## Cómo recompilar el SCSS

```bash
npm install -g sass
sass scss/main.scss styles/styles.css
```

## Despliegue

El sitio está pensado para desplegarse como sitio estático en **Vercel** o
**Netlify** (carpeta raíz como directorio de publicación, sin build step).

## Autor

Gonzalo Corradi — Antares SRL / Trinity Systems.
