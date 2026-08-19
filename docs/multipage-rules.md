# OneMore Multi-Page Rules — Arquitectura, Navegación, Formularios & Transiciones

Reglas para sitios de múltiples páginas: estructura, navegación global, footer, formularios de contacto, SEO meta, y transiciones entre páginas.

---

## 1. Arquitectura de Sitio Estándar

### Tier 2 — Sitio web completo (sin CMS)

```
/                   → Home (landing principal)
/nosotros           → Quiénes somos, historia, equipo
/servicios          → Todos los servicios (overview)
/servicios/[slug]   → Detalle de servicio individual
/galeria            → Galería de fotos / trabajos
/contacto           → Formulario + mapa + horarios
/gracias            → Página de confirmación post-form
```

### Tier 3 — Sitio web + CMS

```
(misma estructura de páginas públicas)
/admin              → Dashboard del administrador
/admin/login        → Login del cliente
/admin/contenido    → Editor de textos/imágenes
/admin/galeria      → Gestión de galería
/admin/servicios    → Gestión de servicios
```

### Reglas de arquitectura

- **NEVER** crear páginas huérfanas (sin enlace desde ningún lugar)
- **ALWAYS** incluir breadcrumbs en páginas de detalle (/servicios/slug)
- **ALWAYS** vincular entre páginas relacionadas (cross-linking)
- **PREFER** URLs en español sin acentos ni caracteres especiales
- **DEFINE** una página 404 personalizada con el menú de navegación

---

## 2. Sticky Navbar Global

Ver `responsive-rules.md` para el código completo del hamburger. Aquí las reglas adicionales para sitios multi-página.

### Estado activo de la página actual

```css
.nav-links a {
  position: relative;
  color: #1d1d1f;
  text-decoration: none;
  font-size: 0.9375rem;
  font-weight: 400;
  transition: color 0.2s ease;
}

/* Subrayado animado en hover */
.nav-links a::after {
  content: '';
  position: absolute;
  bottom: -2px;
  left: 0;
  right: 0;
  height: 1px;
  background: #1d1d1f;
  transform: scaleX(0);
  transform-origin: center;
  transition: transform 0.2s cubic-bezier(0.25, 0.1, 0.25, 1);
}

.nav-links a:hover::after,
.nav-links a[aria-current="page"]::after {
  transform: scaleX(1);
}

/* Página actual — más peso */
.nav-links a[aria-current="page"] {
  font-weight: 500;
}
```

```html
<!-- Marcar página actual con aria-current -->
<a href="/nosotros" aria-current="page">Nosotros</a>
<a href="/servicios">Servicios</a>
```

### Dropdown de servicios (desktop)

```html
<li class="has-dropdown">
  <a href="/servicios" aria-haspopup="true" aria-expanded="false">
    Servicios
    <svg aria-hidden="true" width="10" height="6"><!-- chevron --></svg>
  </a>
  <ul class="dropdown" role="menu">
    <li><a href="/servicios/limpieza" role="menuitem">Limpieza</a></li>
    <li><a href="/servicios/blanqueamiento" role="menuitem">Blanqueamiento</a></li>
    <li><a href="/servicios/ortodoncia" role="menuitem">Ortodoncia</a></li>
  </ul>
</li>
```

```css
.has-dropdown { position: relative; }

.dropdown {
  position: absolute;
  top: calc(100% + 8px);
  left: 0;
  min-width: 200px;
  background: rgba(251, 251, 253, 0.95);
  backdrop-filter: blur(20px);
  border: 0.5px solid rgba(0, 0, 0, 0.1);
  border-radius: 14px;
  padding: 8px;
  list-style: none;
  opacity: 0;
  visibility: hidden;
  transform: translateY(-8px);
  transition: opacity 0.2s ease, transform 0.2s cubic-bezier(0.25, 0.1, 0.25, 1), visibility 0.2s;
  z-index: 200;
}

.has-dropdown:hover .dropdown,
.has-dropdown:focus-within .dropdown {
  opacity: 1;
  visibility: visible;
  transform: translateY(0);
}

.dropdown a {
  display: block;
  padding: 10px 12px;
  border-radius: 8px;
  font-size: 0.875rem;
  color: #1d1d1f;
  text-decoration: none;
  transition: background 0.15s ease;
}

.dropdown a:hover {
  background: rgba(0, 0, 0, 0.05);
}
```

---

## 3. Breadcrumbs

```html
<!-- Schema.org structured data + accesible -->
<nav aria-label="Ruta de navegación" class="breadcrumb">
  <ol itemscope itemtype="https://schema.org/BreadcrumbList">
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <a href="/" itemprop="item"><span itemprop="name">Inicio</span></a>
      <meta itemprop="position" content="1">
    </li>
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <a href="/servicios" itemprop="item"><span itemprop="name">Servicios</span></a>
      <meta itemprop="position" content="2">
    </li>
    <li itemprop="itemListElement" itemscope itemtype="https://schema.org/ListItem">
      <span itemprop="name">Blanqueamiento dental</span>
      <meta itemprop="position" content="3">
    </li>
  </ol>
</nav>
```

```css
.breadcrumb ol {
  display: flex;
  align-items: center;
  gap: 8px;
  list-style: none;
  padding: 0;
  margin: 0;
  flex-wrap: wrap;
}

.breadcrumb li {
  display: flex;
  align-items: center;
  gap: 8px;
  font-size: 0.8125rem;
  color: #6e6e73;
}

/* Separador / */
.breadcrumb li:not(:last-child)::after {
  content: '/';
  color: #adadb0;
}

.breadcrumb a {
  color: #6e6e73;
  text-decoration: none;
  transition: color 0.15s;
}

.breadcrumb a:hover { color: #1d1d1f; }

/* Página actual — sin link */
.breadcrumb li:last-child { color: #1d1d1f; font-weight: 500; }
```

---

## 4. Footer Multi-columna

### Estructura

```html
<footer class="site-footer">
  <div class="footer-container">

    <!-- Columna 1: Marca -->
    <div class="footer-brand">
      <a href="/" class="footer-logo">
        <img src="/logo-white.svg" alt="Empresa" width="120" height="32">
      </a>
      <p class="footer-tagline">Tu descripción breve de máximo 2 líneas.</p>
      <!-- Redes sociales -->
      <div class="social-links" aria-label="Redes sociales">
        <a href="https://instagram.com/empresa" target="_blank" rel="noopener" aria-label="Instagram de Empresa">
          <!-- SVG Instagram -->
        </a>
        <a href="https://wa.me/51999999999" target="_blank" rel="noopener" aria-label="WhatsApp de Empresa">
          <!-- SVG WhatsApp -->
        </a>
      </div>
    </div>

    <!-- Columna 2: Navegación -->
    <nav class="footer-nav" aria-label="Navegación del footer">
      <h3 class="footer-heading">Páginas</h3>
      <ul>
        <li><a href="/">Inicio</a></li>
        <li><a href="/nosotros">Nosotros</a></li>
        <li><a href="/servicios">Servicios</a></li>
        <li><a href="/galeria">Galería</a></li>
        <li><a href="/contacto">Contacto</a></li>
      </ul>
    </nav>

    <!-- Columna 3: Servicios (si aplica) -->
    <nav class="footer-nav" aria-label="Servicios">
      <h3 class="footer-heading">Servicios</h3>
      <ul>
        <li><a href="/servicios/limpieza">Limpieza dental</a></li>
        <li><a href="/servicios/blanqueamiento">Blanqueamiento</a></li>
        <li><a href="/servicios/ortodoncia">Ortodoncia</a></li>
      </ul>
    </nav>

    <!-- Columna 4: Contacto -->
    <div class="footer-contact">
      <h3 class="footer-heading">Contacto</h3>
      <address>
        <p>Av. Principal 123, Lima</p>
        <p><a href="tel:+51999999999">+51 999 999 999</a></p>
        <p><a href="mailto:hola@empresa.com">hola@empresa.com</a></p>
      </address>
      <p class="footer-hours">Lun–Vie: 9am – 7pm<br>Sáb: 9am – 2pm</p>
    </div>

  </div>

  <!-- Bottom bar -->
  <div class="footer-bottom">
    <p class="footer-legal">© 2025 Empresa. Todos los derechos reservados.</p>
    <div class="footer-legal-links">
      <a href="/privacidad">Política de privacidad</a>
      <a href="/terminos">Términos</a>
    </div>
  </div>
</footer>
```

### CSS del footer

```css
.site-footer {
  background: #1d1d1f;
  color: #f5f5f7;
  padding: 64px 20px 32px;
}

@media (min-width: 768px) { .site-footer { padding: 80px 40px 40px; } }
@media (min-width: 1280px) { .site-footer { padding: 96px 80px 48px; } }

.footer-container {
  max-width: 1280px;
  margin: 0 auto;
  display: grid;
  grid-template-columns: 1fr;
  gap: 40px;
}

@media (min-width: 768px) {
  .footer-container {
    grid-template-columns: 1fr 1fr;
    gap: 48px;
  }
}

@media (min-width: 1280px) {
  .footer-container {
    grid-template-columns: 2fr 1fr 1fr 1.5fr;
    gap: 64px;
  }
}

.footer-heading {
  font-size: 0.6875rem;
  font-weight: 600;
  letter-spacing: 0.06em;
  text-transform: uppercase;
  color: #86868b;
  margin-bottom: 16px;
}

.footer-nav ul {
  list-style: none;
  padding: 0;
  margin: 0;
  display: flex;
  flex-direction: column;
  gap: 12px;
}

.footer-nav a {
  color: #f5f5f7;
  text-decoration: none;
  font-size: 0.9375rem;
  transition: color 0.2s;
}

.footer-nav a:hover { color: #d1d1d6; }

.footer-tagline {
  font-size: 0.9375rem;
  color: #86868b;
  line-height: 1.5;
  margin: 12px 0 24px;
}

.social-links {
  display: flex;
  gap: 16px;
}

.social-links a {
  display: flex;
  align-items: center;
  justify-content: center;
  width: 44px;
  height: 44px;
  border-radius: 50%;
  background: rgba(255, 255, 255, 0.08);
  color: #f5f5f7;
  transition: background 0.2s;
  text-decoration: none;
}

.social-links a:hover { background: rgba(255, 255, 255, 0.16); }

/* Contact en footer */
address { font-style: normal; }
address p { font-size: 0.9375rem; color: #f5f5f7; margin: 0 0 8px; }
address a { color: #f5f5f7; text-decoration: none; }
address a:hover { text-decoration: underline; }
.footer-hours { font-size: 0.875rem; color: #86868b; margin-top: 16px; }

/* Bottom bar */
.footer-bottom {
  max-width: 1280px;
  margin: 48px auto 0;
  padding-top: 24px;
  border-top: 0.5px solid rgba(255, 255, 255, 0.1);
  display: flex;
  flex-direction: column;
  gap: 12px;
  align-items: flex-start;
}

@media (min-width: 768px) {
  .footer-bottom {
    flex-direction: row;
    align-items: center;
    justify-content: space-between;
  }
}

.footer-legal { font-size: 0.8125rem; color: #6e6e73; margin: 0; }
.footer-legal-links { display: flex; gap: 20px; }
.footer-legal-links a { font-size: 0.8125rem; color: #6e6e73; text-decoration: none; }
.footer-legal-links a:hover { color: #f5f5f7; }
```

---

## 5. Formulario de Contacto

```html
<form class="contact-form" id="contact-form" novalidate>
  <div class="form-group">
    <label class="form-label" for="name">Nombre completo</label>
    <input
      type="text"
      id="name"
      name="name"
      class="form-input"
      placeholder="Juan García"
      autocomplete="name"
      required
      minlength="2"
    >
    <span class="form-error" id="name-error" role="alert" aria-live="polite"></span>
  </div>

  <div class="form-group">
    <label class="form-label" for="email">Correo electrónico</label>
    <input
      type="email"
      id="email"
      name="email"
      class="form-input"
      placeholder="juan@correo.com"
      autocomplete="email"
      required
    >
    <span class="form-error" id="email-error" role="alert" aria-live="polite"></span>
  </div>

  <div class="form-group">
    <label class="form-label" for="phone">Teléfono (opcional)</label>
    <input
      type="tel"
      id="phone"
      name="phone"
      class="form-input"
      placeholder="+51 999 999 999"
      autocomplete="tel"
    >
  </div>

  <div class="form-group">
    <label class="form-label" for="message">Mensaje</label>
    <textarea
      id="message"
      name="message"
      class="form-input form-textarea"
      placeholder="¿En qué podemos ayudarte?"
      required
      minlength="10"
      rows="5"
    ></textarea>
    <span class="form-error" id="message-error" role="alert" aria-live="polite"></span>
  </div>

  <button type="submit" class="btn-submit" id="submit-btn">
    <span class="btn-text">Enviar mensaje</span>
    <span class="btn-loading" aria-hidden="true" hidden>Enviando…</span>
  </button>

  <p class="form-success" id="form-success" hidden role="status">
    ¡Mensaje enviado! Te contactaremos en menos de 24 horas.
  </p>
</form>
```

### CSS del formulario (Apple style)

```css
.contact-form {
  display: flex;
  flex-direction: column;
  gap: 20px;
  max-width: 560px;
}

.form-group {
  display: flex;
  flex-direction: column;
  gap: 6px;
}

.form-label {
  font-size: 0.8125rem;
  font-weight: 500;
  color: #1d1d1f;
  letter-spacing: 0.01em;
}

.form-input {
  width: 100%;
  min-height: 44px;
  padding: 10px 14px;
  font-size: 1rem;
  font-family: inherit;
  color: #1d1d1f;
  background: #ffffff;
  border: 1px solid rgba(0, 0, 0, 0.18);
  border-radius: 10px;
  outline: none;
  transition: border-color 0.2s ease,
              box-shadow 0.2s ease;
  -webkit-appearance: none;
  appearance: none;
}

.form-input:focus {
  border-color: #0071e3;
  box-shadow: 0 0 0 3px rgba(0, 113, 227, 0.25);
}

/* Estado error */
.form-input.invalid {
  border-color: #ff3b30;
  box-shadow: 0 0 0 3px rgba(255, 59, 48, 0.15);
}

/* Estado válido */
.form-input.valid {
  border-color: #34c759;
}

.form-textarea {
  min-height: 120px;
  resize: vertical;
  line-height: 1.5;
}

.form-error {
  font-size: 0.8125rem;
  color: #ff3b30;
  min-height: 1em; /* Reserva espacio para evitar layout shift */
}

/* Botón submit */
.btn-submit {
  min-height: 50px;
  padding: 12px 32px;
  font-size: 1rem;
  font-weight: 500;
  color: #ffffff;
  background: #1d1d1f;
  border: none;
  border-radius: 980px; /* pill */
  cursor: pointer;
  transition: background 0.2s ease, transform 0.1s ease;
  align-self: flex-start;
}

.btn-submit:hover { background: #3a3a3c; }
.btn-submit:active { transform: scale(0.98); }

.btn-submit:disabled {
  opacity: 0.5;
  cursor: not-allowed;
  transform: none;
}

.form-success {
  padding: 16px;
  background: rgba(52, 199, 89, 0.1);
  border: 1px solid rgba(52, 199, 89, 0.3);
  border-radius: 10px;
  color: #1a7f37;
  font-size: 0.9375rem;
}

/* Dark mode */
@media (prefers-color-scheme: dark) {
  .form-label { color: #f5f5f7; }
  .form-input {
    background: #2c2c2e;
    color: #f5f5f7;
    border-color: rgba(255, 255, 255, 0.15);
  }
  .form-input:focus {
    border-color: #0a84ff;
    box-shadow: 0 0 0 3px rgba(10, 132, 255, 0.25);
  }
  .btn-submit { background: #f5f5f7; color: #1d1d1f; }
  .btn-submit:hover { background: #d1d1d6; }
}
```

### JavaScript de validación en tiempo real

```js
class ContactForm {
  constructor(formId) {
    this.form = document.getElementById(formId);
    if (!this.form) return;
    this.init();
  }

  init() {
    // Validar campo al perder foco
    this.form.querySelectorAll('.form-input').forEach(input => {
      input.addEventListener('blur', () => this.validateField(input));
      input.addEventListener('input', () => {
        if (input.classList.contains('invalid')) this.validateField(input);
      });
    });

    this.form.addEventListener('submit', async (e) => {
      e.preventDefault();
      if (this.validateAll()) await this.submit();
    });
  }

  validateField(input) {
    const errorEl = document.getElementById(`${input.id}-error`);
    let error = '';

    if (input.required && !input.value.trim()) {
      error = 'Este campo es obligatorio.';
    } else if (input.type === 'email' && input.value) {
      const emailRe = /^[^\s@]+@[^\s@]+\.[^\s@]+$/;
      if (!emailRe.test(input.value)) error = 'Ingresa un correo válido.';
    } else if (input.minLength && input.value.length < input.minLength) {
      error = `Mínimo ${input.minLength} caracteres.`;
    }

    input.classList.toggle('invalid', !!error);
    input.classList.toggle('valid', !error && input.value.trim() !== '');
    if (errorEl) errorEl.textContent = error;

    return !error;
  }

  validateAll() {
    const fields = this.form.querySelectorAll('.form-input[required]');
    return Array.from(fields).every(f => this.validateField(f));
  }

  async submit() {
    const btn = this.form.querySelector('#submit-btn');
    const btnText = btn.querySelector('.btn-text');
    const btnLoading = btn.querySelector('.btn-loading');
    const successMsg = document.getElementById('form-success');

    // Estado loading
    btn.disabled = true;
    btnText.hidden = true;
    btnLoading.hidden = false;

    try {
      // Aquí integrar con Formspree, EmailJS, o backend propio
      await new Promise(resolve => setTimeout(resolve, 1500)); // Simular request

      // Estado éxito
      this.form.reset();
      this.form.querySelectorAll('.form-input').forEach(i => {
        i.classList.remove('valid', 'invalid');
      });
      successMsg.hidden = false;
      successMsg.focus();

    } catch (err) {
      alert('Error al enviar. Intenta nuevamente.');
    } finally {
      btn.disabled = false;
      btnText.hidden = false;
      btnLoading.hidden = true;
    }
  }
}

new ContactForm('contact-form');
```

---

## 6. SEO Meta por Página

```html
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">

  <!-- Título: max 60 chars | Keyword primario + Nombre empresa -->
  <title>Servicios de Odontología en Lima | Clínica Dental Nombre</title>

  <!-- Descripción: 150–160 chars, CTA incluido -->
  <meta name="description" content="Limpieza, blanqueamiento y ortodoncia en Lima. Más de 10 años cuidando tu sonrisa. Agenda tu cita hoy — primera consulta gratis.">

  <!-- Open Graph para redes sociales -->
  <meta property="og:type" content="website">
  <meta property="og:title" content="Servicios de Odontología en Lima | Clínica Dental">
  <meta property="og:description" content="Tu descripción de 150 chars aquí.">
  <meta property="og:image" content="https://tudominio.com/og-image.jpg"> <!-- 1200×630 -->
  <meta property="og:url" content="https://tudominio.com/servicios">
  <meta property="og:site_name" content="Clínica Dental Nombre">

  <!-- Twitter Card -->
  <meta name="twitter:card" content="summary_large_image">
  <meta name="twitter:title" content="Servicios de Odontología en Lima">
  <meta name="twitter:description" content="Tu descripción aquí.">
  <meta name="twitter:image" content="https://tudominio.com/og-image.jpg">

  <!-- Canonical para evitar contenido duplicado -->
  <link rel="canonical" href="https://tudominio.com/servicios">

  <!-- Favicon -->
  <link rel="icon" href="/favicon.svg" type="image/svg+xml">
  <link rel="icon" href="/favicon.ico" sizes="any">
  <link rel="apple-touch-icon" href="/apple-touch-icon.png">

  <!-- Schema.org LocalBusiness (en página de inicio y contacto) -->
  <script type="application/ld+json">
  {
    "@context": "https://schema.org",
    "@type": "LocalBusiness",
    "name": "Clínica Dental Nombre",
    "description": "Odontología de alta calidad en Lima",
    "url": "https://tudominio.com",
    "telephone": "+51 999 999 999",
    "address": {
      "@type": "PostalAddress",
      "streetAddress": "Av. Principal 123",
      "addressLocality": "Lima",
      "addressCountry": "PE"
    },
    "openingHours": ["Mo-Fr 09:00-19:00", "Sa 09:00-14:00"],
    "image": "https://tudominio.com/og-image.jpg"
  }
  </script>
</head>
```

---

## 7. Transiciones entre Páginas

### CSS View Transitions API (nativo, sin librerías)

```css
/* En <head> de cada página */
@view-transition { navigation: auto; }

/* Fade suave (predeterminado mejorado) */
::view-transition-old(root) {
  animation: 200ms cubic-bezier(0.25, 0.1, 0.25, 1) both fade-out;
}

::view-transition-new(root) {
  animation: 300ms cubic-bezier(0.25, 0.1, 0.25, 1) both fade-in;
}

@keyframes fade-out {
  to { opacity: 0; transform: translateY(8px); }
}

@keyframes fade-in {
  from { opacity: 0; transform: translateY(8px); }
}

/* Hero compartido entre páginas (shared element transition) */
.page-hero {
  view-transition-name: page-hero;
}

@media (prefers-reduced-motion: reduce) {
  ::view-transition-old(root),
  ::view-transition-new(root) {
    animation: none;
  }
}
```

### Fallback con JavaScript (para navegadores sin View Transitions)

```js
// Fallback simple para navegadores sin View Transitions
if (!document.startViewTransition) {
  document.querySelectorAll('a[href]').forEach(link => {
    // Solo links internos, sin target="_blank"
    if (link.hostname === window.location.hostname && !link.target) {
      link.addEventListener('click', (e) => {
        const href = link.getAttribute('href');
        if (href && !href.startsWith('#') && !href.startsWith('mailto') && !href.startsWith('tel')) {
          e.preventDefault();
          document.body.style.opacity = '0';
          document.body.style.transition = 'opacity 0.2s ease';
          setTimeout(() => { window.location.href = href; }, 200);
        }
      });
    }
  });
}
```

---

## 8. Página 404 Personalizada

```html
<!-- 404.html -->
<section class="error-page">
  <div class="error-container">
    <p class="error-code">404</p>
    <h1 class="error-title">Esta página no existe</h1>
    <p class="error-description">
      La página que buscas fue movida o no existe.<br>
      Vuelve al inicio para encontrar lo que necesitas.
    </p>
    <a href="/" class="btn-primary">Volver al inicio</a>
  </div>
</section>
```

```css
.error-page {
  min-height: 100svh;
  display: flex;
  align-items: center;
  justify-content: center;
  text-align: center;
  padding: 40px 20px;
}

.error-code {
  font-size: clamp(5rem, 20vw, 10rem);
  font-weight: 700;
  color: #f0f0f0;
  line-height: 1;
  margin: 0 0 16px;
}

@media (prefers-color-scheme: dark) {
  .error-code { color: #3a3a3c; }
}

.error-title {
  font-size: clamp(1.5rem, 4vw, 2.5rem);
  font-weight: 600;
  color: #1d1d1f;
  margin: 0 0 16px;
}

.error-description {
  font-size: 1rem;
  color: #6e6e73;
  line-height: 1.6;
  margin: 0 0 32px;
}
```

---

## 9. Anti-Patterns Multi-Página

| Anti-Pattern | Fix |
|---|---|
| Navegar con JS sin preservar historial | Usar `<a href>` real, no `onclick` que cambia innerHTML |
| Footer diferente en cada página | Un solo footer.html incluido en todas las páginas |
| `<title>` igual en todas las páginas | Título único por página: `Página — Sitio` |
| Formulario sin validación client-side | Validar en blur + submit antes de enviar |
| Formulario sin feedback visual | Siempre: loading state + success/error message |
| Links sin `aria-current="page"` | Marcar la página activa en el nav |
| Breadcrumbs sin Schema.org | Siempre incluir structured data en breadcrumbs |
| 404 genérica del servidor | Siempre crear 404.html personalizada con el menú |
| Transición de página abrupta | View Transitions API + fallback fade |

---

## Checklist Multi-Página (antes de entregar)

- [ ] ✅ Todas las páginas tienen `<title>` único y `<meta description>` entre 150–160 chars
- [ ] ✅ Open Graph correcto (og:image es 1200×630px)
- [ ] ✅ `<link rel="canonical">` en todas las páginas
- [ ] ✅ Schema.org LocalBusiness en home y contacto
- [ ] ✅ Navbar marca `aria-current="page"` en página activa
- [ ] ✅ Hamburger funciona con aria-expanded
- [ ] ✅ Footer presente en todas las páginas (idéntico)
- [ ] ✅ Formulario tiene validación + loading state + success message
- [ ] ✅ Breadcrumbs en páginas de detalle (/servicios/slug)
- [ ] ✅ View Transitions o fallback fade entre páginas
- [ ] ✅ 404 personalizada creada
- [ ] ✅ Todos los links externos con `rel="noopener"` + `target="_blank"`
