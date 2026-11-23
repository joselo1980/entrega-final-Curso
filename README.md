# Rodó & Asociados — Proyecto Final

Sitio web estático de 5 páginas del estudio jurídico y notarial Rodó & Asociados, de Parque Rodó, Montevideo. Proyecto Final del curso de Desarrollo Web de Coderhouse.

## Sitio publicado

LINK_DEPLOY

## Páginas

- Inicio (`index.html`)
- Nosotros (`pages/sobre-mi.html`)
- Preguntas frecuentes (`pages/proyectos.html`)
- Servicios (`pages/servicios.html`)
- Contacto (`pages/contacto.html`)

## Estructura

```
index.html
pages/            4 páginas secundarias
assets/img/       imágenes con nombres descriptivos
scss/             estilos en SCSS (partials)
styles/style.css  CSS compilado (no se edita a mano)
```

```
scss/
├── main.scss              (solo @use de los partials)
├── utilities/  _variables.scss, _mixins.scss
├── base/       _base.scss, _tipografia.scss
├── layout/     _header.scss, _nav.scss, _grillas.scss, _footer.scss
└── components/ _buttons.scss, _cards.scss, _carousel.scss, _modal.scss
```

## Cómo se cumple cada requisito

- **HTML semántico:** header, nav, main, section, article y footer en los 5 archivos, un solo h1 por página.
- **SEO:** cada página tiene `<title>`, `<meta name="description">` y `<meta name="keywords">` propios. Todas las imágenes tienen `alt`.
- **Bootstrap 5 (CDN):** navbar con menú hamburguesa en los 5 HTML, carousel en el inicio y modal en Servicios. Estilados desde SCSS con la paleta propia.
- **SCSS:** variables (`_variables.scss`), nesting, mixins con parámetros (`columna($espacio)`, `aparecer($duracion, $demora)`), `@extend` de `%titulo-base` y partials.
- **Responsive (mobile-first):** base sin media query, tablet `@media (min-width: 768px)` y escritorio `@media (min-width: 1024px)`. Sin scroll horizontal de 375px a 1400px.
- **Animaciones:** `@keyframes aparecer` y `transition` en hover (nativas) + librería AOS (`data-aos="fade-up"`).
- **Contraste:** textos sobre fondo azul con dorado claro (5.9:1); textos principales por encima de 9:1.

## Cómo compilar el SCSS

```
npx sass scss/main.scss styles/style.css
```

## Tecnologías

HTML5, SCSS, Bootstrap 5, AOS.
