# OneMore Responsive Rules — 3-Breakpoint System

Sistema de diseño responsive para sitios web de clientes. Tres breakpoints, grids precisos, tipografía fluida, y patrones de navegación móvil.

---

## 1. Breakpoint System

### Definición canónica

```css
/* Mobile first — always write mobile default, then scale up */
:root {
  --bp-mobile: 375px;   /* xs: smartphones portrait */
  --bp-tablet: 768px;   /* md: tablets + smartphones landscape */
  --bp-laptop: 1280px;  /* lg: laptops + desktops */
}

/* Media queries */
@media (min-width: 768px)  { /* tablet+  */ }
@media (min-width: 1280px) { /* laptop+  */ }
```

### Reglas de uso

- **ALWAYS** write mobile styles first, then override with `min-width` queries
- **NEVER** use `max-width` queries for layout (only for edge cases)
- **PREFER** `clamp()` over stepped values when the change is gradual
- **TEST** at 375px (iPhone SE), 390px (iPhone 15), 768px (iPad), 1280px (MacBook Air)
- **AVOID** breakpoints at arbitrary px values — stick to the 3 canonical values

### Tailwind mapping

```
mobile (default) → no prefix
tablet (768px)   → md:
laptop (1280px)  → xl:
```

---

## 2. Grid System

### Columnas por breakpoint

| Breakpoint | Columnas | Gutter | Padding lateral | Max width |
|---|---|---|---|---|
| Mobile (375px) | 4 | 16px | 20px | 100% |
| Tablet (768px) | 8 | 24px | 40px | 100% |
| Laptop (1280px) | 12 | 32px | 80px | 1280px |

### CSS Grid base

```css
.container {
  width: 100%;
  max-width: 1280px;
  margin: 0 auto;
  padding: 0 20px;
}

@media (min-width: 768px) {
  .container { padding: 0 40px; }
}

@media (min-width: 1280px) {
  .container { padding: 0 80px; }
}

.grid {
  display: grid;
  grid-template-columns: repeat(4, 1fr);
  gap: 16px;
}

@media (min-width: 768px) {
  .grid {
    grid-template-columns: repeat(8, 1fr);
    gap: 24px;
  }
}

@media (min-width: 1280px) {
  .grid {
    grid-template-columns: repeat(12, 1fr);
    gap: 32px;
  }
}
```

### Tailwind utility

```html
<!-- 1 col mobile / 2 col tablet / 3 col laptop -->
<div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-3 gap-4 md:gap-6 xl:gap-8">

<!-- 1 col mobile / 2 col tablet / 4 col laptop -->
<div class="grid grid-cols-1 md:grid-cols-2 xl:grid-cols-4 gap-4 md:gap-6 xl:gap-8">

<!-- Full width mobile / 6-of-8 cols tablet / 8-of-12 cols laptop (centered article) -->
<article class="col-span-4 md:col-span-6 md:col-start-2 xl:col-span-8 xl:col-start-3">
```

### Patrones de grid por tipo de sección

```css
/* Hero: siempre full-width */
.section-hero {
  grid-column: 1 / -1;
}

/* Features: 1→2→3 */
.features-grid {
  display: grid;
  grid-template-columns: 1fr;
  gap: 24px;
}
@media (min-width: 768px) {
  .features-grid { grid-template-columns: repeat(2, 1fr); }
}
@media (min-width: 1280px) {
  .features-grid { grid-template-columns: repeat(3, 1fr); }
}

/* Products / Cards: 2→4 */
.cards-grid {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  gap: 16px;
}
@media (min-width: 1280px) {
  .cards-grid {
    grid-template-columns: repeat(4, 1fr);
    gap: 24px;
  }
}

/* Side-by-side content (text + image): stack→split */
.split-section {
  display: grid;
  grid-template-columns: 1fr;
  gap: 40px;
}
@media (min-width: 768px) {
  .split-section {
    grid-template-columns: 1fr 1fr;
    gap: 48px;
    align-items: center;
  }
}
```

---

## 3. Tipografía Fluida

### Escala responsive con clamp()

```css
:root {
  /* Display — hero headlines */
  --text-display-xl: clamp(2.5rem, 8vw, 5rem);     /* 40px→80px */
  --text-display-lg: clamp(2rem, 6vw, 3.5rem);      /* 32px→56px */
  --text-display-md: clamp(1.75rem, 4vw, 2.5rem);   /* 28px→40px */

  /* Headings */
  --text-h1: clamp(1.5rem, 3.5vw, 2.25rem);         /* 24px→36px */
  --text-h2: clamp(1.25rem, 2.5vw, 1.75rem);        /* 20px→28px */
  --text-h3: clamp(1.125rem, 2vw, 1.375rem);        /* 18px→22px */

  /* Body */
  --text-body-lg: clamp(1rem, 1.5vw, 1.125rem);     /* 16px→18px */
  --text-body: 1rem;                                  /* 16px (fixed) */
  --text-sm: 0.875rem;                                /* 14px (fixed) */
  --text-xs: 0.75rem;                                 /* 12px (fixed) */
}

/* Apply */
h1 { font-size: var(--text-h1); }
h2 { font-size: var(--text-h2); }
.hero-headline { font-size: var(--text-display-xl); }
```

### Line heights por breakpoint

```css
/* Mobile: tighter — smaller screens need more vertical space */
p {
  line-height: 1.6;
  font-size: var(--text-body);
}

/* Tablet+: open slightly */
@media (min-width: 768px) {
  p { line-height: 1.65; }
}

/* Headlines always tighter */
h1, h2, h3 { line-height: 1.1; }
.hero-headline { line-height: 1.0; letter-spacing: -0.02em; }
```

---

## 4. Spacing Responsive

### Sección padding (vertical rhythm)

```css
.section {
  padding: 64px 0;
}

@media (min-width: 768px) {
  .section { padding: 96px 0; }
}

@media (min-width: 1280px) {
  .section { padding: 128px 0; }
}

/* Hero always taller */
.section-hero {
  padding: 80px 0 64px;
  min-height: 100svh;
}

@media (min-width: 768px) {
  .section-hero { padding: 120px 0 96px; }
}
```

### Tailwind classes de sección

```html
<!-- Section vertical spacing -->
<section class="py-16 md:py-24 xl:py-32">

<!-- Hero -->
<section class="py-20 md:py-28 xl:py-36 min-h-svh">

<!-- Tight section (footer, cta strip) -->
<section class="py-10 md:py-16 xl:py-20">
```

---

## 5. Hamburger Menu (Mobile Navigation)

### Estructura HTML

```html
<header class="site-header">
  <nav class="navbar">
    <a href="/" class="navbar-brand">
      <img src="/logo.svg" alt="Logo" width="120" height="32">
    </a>

    <!-- Desktop nav — hidden on mobile -->
    <ul class="nav-links" id="nav-links" role="list">
      <li><a href="/servicios">Servicios</a></li>
      <li><a href="/nosotros">Nosotros</a></li>
      <li><a href="/contacto">Contacto</a></li>
    </ul>

    <!-- Desktop CTA -->
    <a href="/contacto" class="btn-primary nav-cta">Cotizar</a>

    <!-- Hamburger — shown only on mobile -->
    <button
      class="hamburger"
      id="hamburger"
      aria-label="Abrir menú"
      aria-expanded="false"
      aria-controls="nav-links"
    >
      <span class="bar"></span>
      <span class="bar"></span>
      <span class="bar"></span>
    </button>
  </nav>
</header>
```

### CSS del hamburger

```css
.site-header {
  position: fixed;
  top: 0;
  left: 0;
  right: 0;
  z-index: 100;
  background: rgba(251, 251, 253, 0.8);
  backdrop-filter: blur(20px) saturate(180%);
  -webkit-backdrop-filter: blur(20px) saturate(180%);
  border-bottom: 0.5px solid rgba(0, 0, 0, 0.08);
  transition: background 0.3s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.navbar {
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 20px;
  height: 56px;
  max-width: 1280px;
  margin: 0 auto;
}

/* Nav links — stack on mobile */
.nav-links {
  display: none;
  flex-direction: column;
  position: fixed;
  inset: 56px 0 0 0;
  background: rgba(251, 251, 253, 0.95);
  backdrop-filter: blur(20px);
  padding: 32px 20px;
  gap: 0;
  list-style: none;
  margin: 0;
}

.nav-links.open {
  display: flex;
}

.nav-links li a {
  display: block;
  padding: 16px 0;
  font-size: 1.25rem;
  font-weight: 500;
  color: #1d1d1f;
  border-bottom: 0.5px solid rgba(0, 0, 0, 0.1);
  text-decoration: none;
}

/* Hamburger icon */
.hamburger {
  display: flex;
  flex-direction: column;
  gap: 5px;
  background: none;
  border: none;
  cursor: pointer;
  padding: 8px;
  min-width: 44px;
  min-height: 44px;
  align-items: center;
  justify-content: center;
}

.bar {
  display: block;
  width: 22px;
  height: 2px;
  background: #1d1d1f;
  border-radius: 2px;
  transition: transform 0.3s cubic-bezier(0.25, 0.1, 0.25, 1),
              opacity 0.2s ease;
}

/* Open state — X animation */
.hamburger[aria-expanded="true"] .bar:nth-child(1) {
  transform: translateY(7px) rotate(45deg);
}
.hamburger[aria-expanded="true"] .bar:nth-child(2) {
  opacity: 0;
  transform: scaleX(0);
}
.hamburger[aria-expanded="true"] .bar:nth-child(3) {
  transform: translateY(-7px) rotate(-45deg);
}

/* Desktop: show nav links inline, hide hamburger */
@media (min-width: 768px) {
  .navbar { padding: 0 40px; height: 64px; }

  .nav-links {
    display: flex;
    flex-direction: row;
    position: static;
    background: none;
    backdrop-filter: none;
    padding: 0;
    gap: 32px;
    align-items: center;
  }

  .nav-links li a {
    font-size: 0.9375rem;
    padding: 0;
    border: none;
  }

  .hamburger { display: none; }
}

@media (min-width: 1280px) {
  .navbar { padding: 0 80px; }
}

/* Dark mode header */
@media (prefers-color-scheme: dark) {
  .site-header {
    background: rgba(29, 29, 31, 0.8);
    border-bottom-color: rgba(255, 255, 255, 0.08);
  }
  .nav-links {
    background: rgba(29, 29, 31, 0.95);
  }
  .nav-links li a { color: #f5f5f7; border-bottom-color: rgba(255,255,255,0.1); }
  .bar { background: #f5f5f7; }
}
```

### JavaScript — toggle sin dependencias

```js
const hamburger = document.getElementById('hamburger');
const navLinks = document.getElementById('nav-links');

hamburger?.addEventListener('click', () => {
  const isOpen = hamburger.getAttribute('aria-expanded') === 'true';
  hamburger.setAttribute('aria-expanded', String(!isOpen));
  navLinks.classList.toggle('open');
  // Prevent body scroll when menu open
  document.body.style.overflow = isOpen ? '' : 'hidden';
});

// Close on link click (mobile)
navLinks?.querySelectorAll('a').forEach(link => {
  link.addEventListener('click', () => {
    hamburger.setAttribute('aria-expanded', 'false');
    navLinks.classList.remove('open');
    document.body.style.overflow = '';
  });
});

// Close on resize to tablet+
window.addEventListener('resize', () => {
  if (window.innerWidth >= 768) {
    hamburger.setAttribute('aria-expanded', 'false');
    navLinks.classList.remove('open');
    document.body.style.overflow = '';
  }
});
```

---

## 6. Sticky Header con Scroll State

```js
const header = document.querySelector('.site-header');
let lastScrollY = 0;

window.addEventListener('scroll', () => {
  const currentScrollY = window.scrollY;

  // Add scrolled class after 10px
  header.classList.toggle('scrolled', currentScrollY > 10);

  // Hide on scroll down, show on scroll up
  if (currentScrollY > lastScrollY && currentScrollY > 80) {
    header.classList.add('hidden');
  } else {
    header.classList.remove('hidden');
  }

  lastScrollY = currentScrollY;
}, { passive: true });
```

```css
.site-header {
  transition: transform 0.3s cubic-bezier(0.25, 0.1, 0.25, 1),
              background 0.3s ease;
}

.site-header.scrolled {
  /* More opaque when scrolled */
  background: rgba(251, 251, 253, 0.92);
}

.site-header.hidden {
  transform: translateY(-100%);
}
```

---

## 7. Touch Targets en Mobile

```css
/* ALWAYS 44px minimum — Apple HIG requirement */
a, button, [role="button"] {
  min-height: 44px;
  min-width: 44px;
}

/* Nav links need extra padding on mobile */
.nav-links li a {
  padding: 14px 0;  /* ensures 44px+ touch target */
}

/* Icon buttons — use padding to extend hit area */
.icon-btn {
  padding: 10px;  /* extends 24px icon to 44px touch target */
}
```

---

## 8. Visibility Utilities

```css
/* Hide on mobile, show on tablet+ */
.hide-mobile { display: none; }
@media (min-width: 768px) { .hide-mobile { display: block; } }

/* Show on mobile, hide on tablet+ */
.show-mobile { display: block; }
@media (min-width: 768px) { .show-mobile { display: none; } }

/* Text alignment responsive */
.text-center-mobile { text-align: center; }
@media (min-width: 768px) { .text-center-mobile { text-align: left; } }
```

---

## 9. Reduced Motion — Responsive Animations

```css
/* ALWAYS include this for every animation */
@media (prefers-reduced-motion: reduce) {
  *,
  *::before,
  *::after {
    animation-duration: 0.01ms !important;
    animation-iteration-count: 1 !important;
    transition-duration: 0.01ms !important;
    scroll-behavior: auto !important;
  }
}
```

---

## 10. Anti-Patterns Responsive

| Anti-Pattern | Fix |
|---|---|
| Fixed widths en px | Usar `%`, `vw`, `fr`, `clamp()` |
| `max-width` media queries | Mobile-first con `min-width` |
| Breakpoint en valores raros (600px, 992px) | Solo 768px y 1280px |
| Font size fijo en mobile | `clamp()` para display, fixed solo para body |
| 3+ columnas en mobile | Máximo 2 columnas en 375px (cards pequeñas) |
| `vh` para hero en mobile | Usar `svh` (safe viewport height) |
| Overflow horizontal | `overflow-x: hidden` en body solo si necesario |
| Hamburger sin aria-expanded | Siempre con aria attributes correctos |
| Touch targets <44px | Siempre min 44px height + width |

---

## Checklist Responsive (antes de entregar)

- [ ] ✅ Testar en 375px — ¿hay overflow horizontal?
- [ ] ✅ Testar en 768px — ¿el grid está correcto?
- [ ] ✅ Testar en 1280px — ¿max-width respetado?
- [ ] ✅ Hamburger funciona + aria correcto
- [ ] ✅ Touch targets ≥44px en todos los interactivos
- [ ] ✅ Imágenes no se desbordan (`max-width: 100%`)
- [ ] ✅ Texto legible sin zoom en 375px (≥16px body)
- [ ] ✅ Header no tapa contenido (padding-top en body igual a header height)
- [ ] ✅ Footer legible en mobile (no 3 columnas apiladas ilegibles)
- [ ] ✅ `prefers-reduced-motion` incluido
