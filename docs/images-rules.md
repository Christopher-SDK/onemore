# OneMore Images Rules — Fotografía, Responsive Images & Performance

Reglas para el uso correcto de imágenes en sitios de clientes. Aspect ratios, lazy loading, placeholders, art direction, retina, y accesibilidad.

---

## 1. Formato Correcto por Caso de Uso

| Caso | Formato | Razón |
|---|---|---|
| Fotografías | WebP + JPEG fallback | Mejor compresión, amplio soporte |
| Ilustraciones / gráficos con transparencia | WebP + PNG fallback | Transparencia sin pérdida |
| Logos / iconos escalables | SVG | Vector, cualquier resolución |
| Íconos de UI (14–24px) | SVG inline o icon font | No depende de red |
| Animaciones simples | GIF → WebP animado | WebP animado es 3x más liviano |
| Screenshots de producto | WebP 2x | Nitidez en retina |

### Regla WebP con fallback (siempre)

```html
<!-- CORRECTO: picture + source WebP + img JPEG -->
<picture>
  <source srcset="imagen.webp" type="image/webp">
  <img src="imagen.jpg" alt="Descripción" width="800" height="600" loading="lazy">
</picture>

<!-- INCORRECTO: solo img sin source WebP -->
<img src="imagen.jpg" alt="...">
```

---

## 2. Aspect Ratios por Sección

### Estándar por tipo de sección

| Sección | Mobile | Tablet | Desktop | CSS |
|---|---|---|---|---|
| Hero background | 4:5 (vertical) | 16:9 | 16:9 | `aspect-ratio: 16/9` |
| Hero producto (mockup) | 1:1 | 4:3 | 3:2 | `aspect-ratio: 3/2` |
| Card (producto/servicio) | 3:2 | 4:3 | 3:2 | `aspect-ratio: 3/2` |
| Card cuadrada | 1:1 | 1:1 | 1:1 | `aspect-ratio: 1/1` |
| Thumbnail / miniatura | 16:9 | 16:9 | 16:9 | `aspect-ratio: 16/9` |
| Team / avatar | 1:1 | 1:1 | 1:1 | `aspect-ratio: 1/1` |
| Logo cliente | libre | libre | libre | `max-height: 40px` |
| Galería | 4:3 | 4:3 | 4:3 | `aspect-ratio: 4/3` |
| Banner ancho | 3:1 | 4:1 | 5:1 | `aspect-ratio: 5/1` |

### CSS — reservar espacio ANTES de cargar (previene CLS)

```css
/* SIEMPRE definir aspect-ratio para prevenir layout shift */
.hero-img-wrapper {
  aspect-ratio: 16 / 9;
  overflow: hidden;
}

.card-img-wrapper {
  aspect-ratio: 3 / 2;
  overflow: hidden;
}

.avatar {
  aspect-ratio: 1 / 1;
  border-radius: 50%;
  overflow: hidden;
}

/* Imagen rellena el contenedor sin distorsionar */
.hero-img-wrapper img,
.card-img-wrapper img,
.avatar img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  object-position: center;
}
```

---

## 3. Retina / HiDPI — srcset

```html
<!-- srcset 1x / 2x para imágenes fijas -->
<img
  src="producto-400.jpg"
  srcset="producto-400.jpg 1x, producto-800.jpg 2x"
  alt="Descripción del producto"
  width="400"
  height="300"
>

<!-- srcset + sizes para imágenes que cambian tamaño con el viewport -->
<picture>
  <source type="image/webp"
    srcset="hero-mobile.webp 768w, hero-tablet.webp 1280w, hero-desktop.webp 1920w"
    sizes="(max-width: 768px) 100vw, (max-width: 1280px) 100vw, 1280px"
  >
  <img
    src="hero-desktop.jpg"
    srcset="hero-mobile.jpg 768w, hero-tablet.jpg 1280w, hero-desktop.jpg 1920w"
    sizes="(max-width: 768px) 100vw, (max-width: 1280px) 100vw, 1280px"
    alt="Hero de la empresa"
    width="1920"
    height="1080"
  >
</picture>
```

### Tamaños de exportación recomendados

| Tipo | Mobile | Tablet | Desktop | Retina desktop |
|---|---|---|---|---|
| Hero | 768×432 | 1280×720 | 1920×1080 | 2560×1440 |
| Card | 400×267 | 600×400 | 800×533 | 1600×1067 |
| Avatar | 80×80 | 80×80 | 120×120 | 240×240 |
| Logo | SVG | SVG | SVG | SVG |

---

## 4. Art Direction por Breakpoint

Usar `<picture>` con `<source media>` para servir imágenes completamente distintas según pantalla.

```html
<!-- Art direction: imagen diferente en mobile vs desktop -->
<picture>
  <!-- Mobile: foto vertical o cuadrada, crop centrado en sujeto -->
  <source
    media="(max-width: 767px)"
    srcset="hero-mobile.webp"
    type="image/webp"
  >
  <source
    media="(max-width: 767px)"
    srcset="hero-mobile.jpg"
  >

  <!-- Tablet: versión intermedia -->
  <source
    media="(max-width: 1279px)"
    srcset="hero-tablet.webp"
    type="image/webp"
  >

  <!-- Desktop: foto panorámica -->
  <source srcset="hero-desktop.webp" type="image/webp">

  <!-- Fallback siempre al final -->
  <img
    src="hero-desktop.jpg"
    alt="Interior del local con luz natural"
    width="1920"
    height="1080"
  >
</picture>
```

### Cuándo usar art direction

- Hero con sujeto en el costado → en mobile recortar para centrar el sujeto
- Producto con contexto amplio → en mobile mostrar solo el producto
- Foto de equipo grupal → en mobile versión más estrecha o primer plano
- Infografía horizontal → en mobile mostrar versión vertical

---

## 5. Lazy Loading

```html
<!-- SIEMPRE lazy para imágenes below the fold -->
<img
  src="producto.jpg"
  alt="Descripción"
  width="400"
  height="267"
  loading="lazy"
  decoding="async"
>

<!-- NUNCA lazy para imágenes LCP (above the fold, hero) -->
<img
  src="hero.jpg"
  alt="Hero"
  width="1920"
  height="1080"
  loading="eager"
  fetchpriority="high"
>
```

### Preload del LCP (en `<head>`)

```html
<!-- Precargar imagen hero para acelerar LCP -->
<link
  rel="preload"
  as="image"
  href="hero-desktop.webp"
  imagesrcset="hero-mobile.webp 768w, hero-tablet.webp 1280w, hero-desktop.webp 1920w"
  imagesizes="100vw"
>
```

### Lazy loading con IntersectionObserver (para galerías)

```js
// Para galerías con muchas imágenes — observar cada una
const images = document.querySelectorAll('img[data-src]');

const observer = new IntersectionObserver((entries) => {
  entries.forEach(entry => {
    if (entry.isIntersecting) {
      const img = entry.target;
      img.src = img.dataset.src;
      if (img.dataset.srcset) img.srcset = img.dataset.srcset;
      img.removeAttribute('data-src');
      observer.unobserve(img);
    }
  });
}, {
  rootMargin: '200px 0px' // Precargar 200px antes de que sea visible
});

images.forEach(img => observer.observe(img));
```

```html
<!-- Uso con data-src para lazy manual -->
<img
  data-src="producto.webp"
  src="data:image/gif;base64,R0lGODlhAQABAIAAAAAAAP///yH5BAEAAAAALAAAAAABAAEAAAIBRAA7"
  alt="Producto"
  width="400"
  height="267"
>
```

---

## 6. Placeholder States — mientras carga

### Blur-up (efecto de desenfoque progresivo)

```css
.img-wrapper {
  position: relative;
  overflow: hidden;
  background: #f0eeeb; /* color base mientras no carga */
}

.img-blur {
  filter: blur(20px);
  transform: scale(1.05); /* evita bordes blancos del blur */
  transition: filter 0.4s cubic-bezier(0.25, 0.1, 0.25, 1),
              transform 0.4s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.img-blur.loaded {
  filter: blur(0);
  transform: scale(1);
}
```

```js
// Activar transición cuando la imagen carga
document.querySelectorAll('.img-blur').forEach(img => {
  if (img.complete) {
    img.classList.add('loaded');
  } else {
    img.addEventListener('load', () => img.classList.add('loaded'));
  }
});
```

### Skeleton placeholder

```css
.img-skeleton {
  background: linear-gradient(
    90deg,
    #f0eeeb 25%,
    #e8e6e3 50%,
    #f0eeeb 75%
  );
  background-size: 200% 100%;
  animation: skeleton-shimmer 1.5s ease-in-out infinite;
  border-radius: inherit;
}

@keyframes skeleton-shimmer {
  0%   { background-position: 200% 0; }
  100% { background-position: -200% 0; }
}

/* Dark mode skeleton */
@media (prefers-color-scheme: dark) {
  .img-skeleton {
    background: linear-gradient(
      90deg,
      #3a3a3c 25%,
      #48484a 50%,
      #3a3a3c 75%
    );
    background-size: 200% 100%;
  }
}

/* Respetar prefers-reduced-motion */
@media (prefers-reduced-motion: reduce) {
  .img-skeleton { animation: none; background: #f0eeeb; }
}
```

---

## 7. Alt Text — Accesibilidad

### Reglas de redacción

```html
<!-- Fotografía descriptiva — describe lo que se ve -->
<img src="cafe.jpg" alt="Taza de café con leche sobre mesa de madera con libro abierto">

<!-- Imagen de producto — nombre + característica clave -->
<img src="croissant.jpg" alt="Croissant de mantequilla recién horneado">

<!-- Foto de persona del equipo -->
<img src="maria.jpg" alt="María López, fundadora de Organico Café, sonriendo en la cocina">

<!-- Ícono / imagen decorativa — alt vacío (no se anuncia con screen reader) -->
<img src="divider.svg" alt="" aria-hidden="true">

<!-- Logo de empresa -->
<img src="logo.svg" alt="Organico Café — Cafetería artesanal en Villa El Salvador">

<!-- NUNCA: alt genérico -->
<img src="foto.jpg" alt="imagen"> <!-- INCORRECTO -->
<img src="foto.jpg" alt="foto de nuestra empresa"> <!-- INCORRECTO -->
```

### Longitud recomendada

- Alt text: máximo 125 caracteres
- Si la imagen tiene texto visible → incluir ese texto en el alt
- Si la imagen es compleja (infografía) → usar `aria-describedby` con descripción larga cercana

---

## 8. Imágenes de Galería

```html
<!-- Galería responsive con lightbox (sin dependencias) -->
<div class="gallery" role="list">
  <figure class="gallery-item" role="listitem">
    <a href="foto-1-full.jpg" class="gallery-trigger" data-lightbox>
      <picture>
        <source srcset="foto-1-thumb.webp" type="image/webp">
        <img
          src="foto-1-thumb.jpg"
          alt="Interior del local en horario de mañana"
          width="400"
          height="300"
          loading="lazy"
        >
      </picture>
    </a>
    <figcaption class="gallery-caption">Local en la mañana</figcaption>
  </figure>
</div>
```

```css
.gallery {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 8px;
}

@media (min-width: 768px) {
  .gallery { grid-template-columns: repeat(3, 1fr); gap: 12px; }
}

@media (min-width: 1280px) {
  .gallery { grid-template-columns: repeat(4, 1fr); gap: 16px; }
}

.gallery-item {
  aspect-ratio: 4 / 3;
  overflow: hidden;
  border-radius: 12px;
}

.gallery-item img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.gallery-item:hover img {
  transform: scale(1.05);
}

.gallery-caption {
  font-size: 0.75rem;
  color: #6e6e73;
  padding: 8px 0;
}
```

---

## 9. Dark Mode — Imágenes con tema

```html
<!-- Mostrar imagen diferente según tema -->
<picture>
  <source
    srcset="logo-dark.webp"
    media="(prefers-color-scheme: dark)"
    type="image/webp"
  >
  <source
    srcset="logo-light.webp"
    type="image/webp"
  >
  <img src="logo-light.png" alt="Logo empresa" width="160" height="40">
</picture>
```

```css
/* Atenuar imágenes en dark mode (evitar que "brillen") */
@media (prefers-color-scheme: dark) {
  img:not([src$=".svg"]) {
    filter: brightness(0.85) contrast(1.05);
  }

  /* Excepciones: logos y product shots no se atenúan */
  .logo img,
  .product-img img {
    filter: none;
  }
}
```

---

## 10. Performance — Reglas Críticas

```html
<!-- LCP image: eager + fetchpriority high + preload en <head> -->
<img
  src="hero.webp"
  alt="..."
  width="1920"
  height="1080"
  loading="eager"
  fetchpriority="high"
  decoding="sync"
>

<!-- Below fold: lazy + async decoding -->
<img
  src="seccion.webp"
  alt="..."
  width="800"
  height="600"
  loading="lazy"
  decoding="async"
>
```

```css
/* SIEMPRE definir width + height para evitar CLS */
img {
  max-width: 100%;
  height: auto; /* mantiene aspect ratio */
}

/* Solo cuando el contenedor controla el tamaño */
.img-fill {
  width: 100%;
  height: 100%;
  object-fit: cover;
}
```

### Tamaños máximos recomendados (antes de servir)

| Tipo | Max KB |
|---|---|
| Hero desktop (WebP) | 150–250 KB |
| Hero mobile (WebP) | 60–100 KB |
| Card thumbnail (WebP) | 20–50 KB |
| Avatar (WebP) | 5–15 KB |
| Logo (SVG) | 2–10 KB |

---

## 11. Anti-Patterns de Imágenes

| Anti-Pattern | Fix |
|---|---|
| `<img src="foto.jpg">` sin width/height | Siempre incluir width + height |
| JPEG/PNG sin WebP | Siempre `<picture>` + `<source>` WebP |
| Hero con `loading="lazy"` | Hero LCP: `loading="eager"` + `fetchpriority="high"` |
| Alt vacío en imagen informativa | Describir el contenido |
| Alt "imagen de..." | Directo al contenido: "Croissant de mantequilla" |
| Imagen decorativa con alt descriptivo | `alt=""` + `aria-hidden="true"` |
| Imágenes de 3MB en producción | Comprimir a <250KB para hero, <50KB para cards |
| `object-fit: stretch` | Siempre `object-fit: cover` o `contain` |
| Sin `aspect-ratio` en contenedor | Definir aspect-ratio para prevenir CLS |

---

## Checklist de Imágenes (antes de entregar)

- [ ] ✅ Todas las imágenes tienen `width` + `height` definidos
- [ ] ✅ Hero image: `loading="eager"` + `fetchpriority="high"`
- [ ] ✅ Imágenes below fold: `loading="lazy"` + `decoding="async"`
- [ ] ✅ `<picture>` con `<source>` WebP en todas las fotografías
- [ ] ✅ Alt text descriptivo en todas las imágenes informativas
- [ ] ✅ Imágenes decorativas con `alt=""` + `aria-hidden="true"`
- [ ] ✅ `aspect-ratio` definido en contenedor (previene CLS)
- [ ] ✅ `object-fit: cover` en imágenes con contenedor fijo
- [ ] ✅ Placeholder/skeleton visible mientras carga (si hay imágenes pesadas)
- [ ] ✅ Tamaños de archivo optimizados (<250KB hero, <50KB cards)
