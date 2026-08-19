# OneMore Business Patterns — Patrones por Industria

Secciones estándar, paletas, y componentes específicos para 10 tipos de negocio local. Cada industria tiene sus secciones obligatorias, paleta base, y componentes especiales.

---

## Cómo usar este archivo

Para cada cliente, identificar su industria y aplicar:
1. **Secciones obligatorias** — la estructura de la página
2. **Paleta base** — colores que transmiten la identidad del sector
3. **Componentes especiales** — los elementos únicos de esa industria
4. **CTA principal** — la acción más valiosa para el negocio

Luego combinar con las reglas de `craft-rules.md`, `responsive-rules.md`, e `images-rules.md`.

---

## 1. Cafetería / Panadería / Restaurante

### Secciones (en orden)

1. **Hero** — foto ambiente del local, titular emocional, botón "Ver menú" o "Reservar"
2. **Propuesta** — 3 razones de por qué este lugar (ingredientes, ambiente, historia)
3. **Carta / Especialidades** — 4–6 platos/bebidas destacados con foto, nombre, precio
4. **Historia** — párrafo del fundador, foto de la cocina o del equipo
5. **Galería** — 8–12 fotos del local, platos, momentos
6. **Horarios y Ubicación** — tabla de horarios + mapa embebido
7. **Instagram feed** — últimas 6 fotos (o placeholder con link al perfil)
8. **CTA final** — "Visítanos" con dirección destacada o botón de WhatsApp

### Paleta base

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Artesanal/orgánico | `#5C3D2E` (café) | `#2D4A35` (verde bosque) | `#D4A853` (dorado) | `#F5EDD8` (crema) |
| Moderno/minimalista | `#1d1d1f` (negro) | `#6e6e73` (gris) | `#FF9F0A` (ámbar) | `#fbfbfd` (blanco) |
| Mediterráneo | `#8B3A2A` (terracota) | `#1A3C40` (verde oscuro) | `#E8C17A` (trigo) | `#FDF6EC` (marfil) |

### Componentes especiales

```html
<!-- Carta con precio -->
<article class="menu-item">
  <div class="menu-item-img">
    <picture>
      <source srcset="croissant.webp" type="image/webp">
      <img src="croissant.jpg" alt="Croissant de mantequilla" width="300" height="200" loading="lazy">
    </picture>
  </div>
  <div class="menu-item-info">
    <h3 class="menu-item-name">Croissant de mantequilla</h3>
    <p class="menu-item-desc">Elaborado con masa madre, horneado cada mañana.</p>
    <p class="menu-item-price">S/ 8.50</p>
  </div>
</article>

<!-- Horarios de atención -->
<table class="hours-table" aria-label="Horarios de atención">
  <caption class="sr-only">Horarios de la semana</caption>
  <tbody>
    <tr>
      <th scope="row">Lunes – Viernes</th>
      <td>7:00 am – 8:00 pm</td>
    </tr>
    <tr>
      <th scope="row">Sábado</th>
      <td>7:00 am – 6:00 pm</td>
    </tr>
    <tr>
      <th scope="row">Domingo</th>
      <td>8:00 am – 2:00 pm</td>
    </tr>
  </tbody>
</table>
```

### CTA principal

```html
<!-- WhatsApp — el CTA más efectivo para negocios locales en Perú -->
<a
  href="https://wa.me/51999999999?text=Hola,%20deseo%20hacer%20un%20pedido"
  class="btn-whatsapp"
  target="_blank"
  rel="noopener"
  aria-label="Pedir por WhatsApp"
>
  <svg aria-hidden="true"><!-- WhatsApp icon --></svg>
  Pedir por WhatsApp
</a>
```

```css
.btn-whatsapp {
  display: inline-flex;
  align-items: center;
  gap: 10px;
  padding: 14px 28px;
  background: #25D366;
  color: #fff;
  border-radius: 980px;
  font-size: 1rem;
  font-weight: 500;
  text-decoration: none;
  min-height: 50px;
  transition: background 0.2s;
}

.btn-whatsapp:hover { background: #1ebe5a; }
```

---

## 2. Odontología / Clínica Dental

### Secciones (en orden)

1. **Hero** — ambiente moderno de la clínica, titular de transformación, botón "Agendar cita"
2. **Servicios** — 6 servicios principales en grid de cards (con ícono, nombre, breve descripción)
3. **¿Por qué elegirnos?** — 3–4 diferenciadores (tecnología, años de experiencia, garantía)
4. **Antes y Después** — galería de casos con slider (tab: Antes / Después)
5. **Equipo** — fotos del/los dentistas con nombre, especialidad, años de experiencia
6. **Proceso** — 4 pasos de cómo funciona (consulta → plan → tratamiento → seguimiento)
7. **Testimonios** — 3–5 reseñas reales con foto, nombre, tratamiento recibido, estrellas
8. **Preguntas Frecuentes** — accordion con 5–7 preguntas comunes
9. **Ubicación + CTA** — mapa, horarios, botón de cita

### Paleta base

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Confianza/salud | `#0A84FF` (azul Apple) | `#34C759` (verde) | `#5AC8FA` (celeste) | `#fbfbfd` (blanco) |
| Sofisticado | `#1d1d1f` (negro) | `#0071E3` (azul) | `#5856D6` (índigo) | `#fbfbfd` (blanco) |
| Fresco/limpio | `#2C7BB6` (azul médico) | `#27AE60` (verde) | `#F39C12` (naranja suave) | `#F0F8FF` (azul muy claro) |

### Componentes especiales

```html
<!-- Card de servicio con ícono -->
<article class="service-card">
  <div class="service-icon" aria-hidden="true">
    <!-- SVG del ícono del servicio -->
  </div>
  <h3 class="service-name">Blanqueamiento dental</h3>
  <p class="service-desc">Recupera el brillo natural de tus dientes en una sola sesión con tecnología LED de última generación.</p>
  <a href="/servicios/blanqueamiento" class="service-link">
    Ver más <span aria-hidden="true">→</span>
  </a>
</article>

<!-- Antes/Después slider -->
<div class="before-after" style="--split: 50%">
  <div class="before">
    <img src="caso-antes.jpg" alt="Antes del tratamiento de ortodoncia" width="600" height="400" loading="lazy">
    <span class="ba-label">Antes</span>
  </div>
  <div class="after">
    <img src="caso-despues.jpg" alt="Después del tratamiento de ortodoncia" width="600" height="400" loading="lazy">
    <span class="ba-label">Después</span>
  </div>
  <input
    type="range"
    class="ba-slider"
    min="0" max="100" value="50"
    aria-label="Deslizar para comparar antes y después"
  >
</div>

<!-- Card de testimonio -->
<article class="testimonial-card">
  <div class="testimonial-stars" aria-label="5 de 5 estrellas">
    ★★★★★
  </div>
  <blockquote class="testimonial-text">
    "Cambió mi sonrisa completamente. El proceso fue rápido y sin dolor. Los recomiendo al 100%."
  </blockquote>
  <footer class="testimonial-author">
    <img src="paciente-maria.jpg" alt="María P." width="48" height="48" loading="lazy">
    <div>
      <cite class="testimonial-name">María P.</cite>
      <p class="testimonial-treatment">Blanqueamiento + Ortodoncia</p>
    </div>
  </footer>
</article>

<!-- FAQ Accordion -->
<details class="faq-item">
  <summary class="faq-question">¿La primera consulta tiene costo?</summary>
  <p class="faq-answer">
    La primera consulta de evaluación es completamente gratuita. Agenda tu cita sin compromiso.
  </p>
</details>
```

---

## 3. Consultora / Empresa de Servicios Profesionales

### Secciones (en orden)

1. **Hero** — tagline de resultado, no de servicio. Botón "Agendar llamada gratuita"
2. **Problema** — nombrar el dolor que resuelven (sin rodeos)
3. **Solución / Servicios** — 3–4 servicios en cards con icono y descripción de resultado
4. **Proceso** — cómo trabajan en 4 pasos claros
5. **Casos de éxito / Resultados** — 2–3 casos con número de resultado (no historia larga)
6. **Clientes** — logos de empresas clientes (máximo 8, en fila con autoplay)
7. **Equipo** — fundadores / partners con foto y especialidad
8. **CTA** — llamada o formulario de contacto directo

### Paleta base

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Autoridad/confianza | `#1d1d1f` (negro) | `#0071E3` (azul) | `#5856D6` (índigo) | `#fbfbfd` |
| Energía/innovación | `#5856D6` (índigo) | `#FF2D55` (rojo Apple) | `#FF9F0A` (ámbar) | `#fbfbfd` |
| Corporativo premium | `#1C3557` (azul marino) | `#C8A85E` (dorado) | `#E8E8E8` (gris) | `#FAFAF9` |

### Componentes especiales

```html
<!-- Stat de resultado — impacto visual -->
<div class="result-stat">
  <span class="stat-number" data-target="340">0</span>
  <span class="stat-suffix">%</span>
  <p class="stat-label">de ROI promedio en 6 meses</p>
</div>

<!-- Case study compacto -->
<article class="case-study">
  <img src="cliente-logo.svg" alt="Logo de empresa cliente" height="32" loading="lazy">
  <blockquote class="case-quote">
    "Redujimos costos operativos en 45% en el primer trimestre."
  </blockquote>
  <p class="case-result">
    <strong>↓45%</strong> costos operativos · <strong>3x</strong> velocidad de proceso
  </p>
</article>
```

---

## 4. Gimnasio / Centro de Fitness

### Secciones (en orden)

1. **Hero** — video o foto de alta energía, titular motivacional, "Prueba gratis 7 días"
2. **Disciplinas** — cards de cada disciplina (yoga, HIIT, boxing, etc.)
3. **Instalaciones** — galería de equipos, áreas, vestuarios
4. **Entrenadores** — equipo con foto, nombre, especialidad, certificaciones
5. **Planes y precios** — tabla comparativa de membresías (3 tiers: básico/estándar/premium)
6. **Horarios** — tabla de clases de la semana
7. **Transformaciones** — antes/después de miembros reales (con consentimiento)
8. **CTA** — "Empieza hoy" con formulario o WhatsApp

### Paleta base

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Energía/potencia | `#FF2D55` (rojo) | `#1d1d1f` (negro) | `#FF9F0A` (naranja) | `#1d1d1f` (oscuro) |
| Salud/bienestar | `#34C759` (verde) | `#30B0C7` (teal) | `#FFD60A` (amarillo) | `#fbfbfd` |
| Premium/luxury | `#B8860B` (dorado) | `#1d1d1f` (negro) | `#C0C0C0` (plata) | `#0a0a0a` (negro puro) |

### Componentes especiales

```html
<!-- Tabla de precios (pricing) -->
<div class="pricing-grid">
  <article class="pricing-card">
    <h3 class="plan-name">Básico</h3>
    <div class="plan-price">
      <span class="price-amount">S/ 89</span>
      <span class="price-period">/mes</span>
    </div>
    <ul class="plan-features">
      <li>✓ Acceso de Lun–Vie (6am–9pm)</li>
      <li>✓ Zona cardio y pesas</li>
      <li>✗ Clases grupales</li>
      <li>✗ Entrenador personal</li>
    </ul>
    <a href="/contacto" class="btn-plan">Empezar</a>
  </article>

  <article class="pricing-card pricing-card--featured">
    <span class="plan-badge">Más popular</span>
    <h3 class="plan-name">Estándar</h3>
    <div class="plan-price">
      <span class="price-amount">S/ 149</span>
      <span class="price-period">/mes</span>
    </div>
    <ul class="plan-features">
      <li>✓ Acceso ilimitado 7 días</li>
      <li>✓ Zona cardio y pesas</li>
      <li>✓ 10 clases grupales/mes</li>
      <li>✗ Entrenador personal</li>
    </ul>
    <a href="/contacto" class="btn-plan btn-plan--primary">Empezar</a>
  </article>
</div>
```

---

## 5. Salón de Belleza / Spa

### Secciones (en orden)

1. **Hero** — foto de ambiente lujoso o íntimo, titular de experiencia/bienestar
2. **Servicios** — grid de servicios con foto, nombre y precio desde
3. **Experiencia** — storytelling del proceso (qué se siente visitarlos)
4. **Equipo** — estilistas/terapeutas con nombre y especialidad
5. **Galería** — antes/después de cortes, coloraciones, etc.
6. **Reseñas** — Google Reviews (3 estrellas + texto)
7. **Reservas** — botón Calendly embebido o WhatsApp para citas

### Paleta base

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Femenino/elegante | `#C9A882` (nude) | `#5C4B3E` (marrón) | `#F8D7DA` (rosa suave) | `#FDF8F5` (crema) |
| Moderno/unisex | `#1d1d1f` (negro) | `#86868b` (gris) | `#BF5AF2` (morado) | `#fbfbfd` |
| Natural/orgánico | `#4A7C59` (verde salvia) | `#8B6914` (tierra) | `#E8C17A` (dorado) | `#F5F0E8` (lino) |

---

## 6. Abogados / Estudio Jurídico

### Secciones (en orden)

1. **Hero** — titular de resultado ("Protegemos lo que construiste"), no de servicio
2. **Áreas de práctica** — 4–6 áreas con ícono y descripción corta
3. **Por qué nosotros** — diferenciadores (experiencia, resultados, disponibilidad)
4. **Proceso** — 4 pasos simples del trabajo conjunto
5. **Equipo** — socios y abogados con foto profesional, colegiatura, áreas
6. **Resultados / Casos** — estadísticas anónimas o testimonios genéricos
7. **Consulta gratuita** — formulario corto o WhatsApp

### Paleta base (siempre seria, nunca colorida)

| Estilo | Primario | Secundario | Acento | Fondo |
|---|---|---|---|---|
| Autoridad clásica | `#1C2E4A` (azul marino) | `#8B7355` (cuero) | `#C5A028` (dorado) | `#F9F7F4` (pergamino) |
| Moderno/accesible | `#1d1d1f` (negro) | `#0071E3` (azul) | `#34C759` (verde éxito) | `#fbfbfd` |

### Reglas específicas

- **NEVER** usar colores llamativos o juguetonesçn — el cliente confía, no compra un entretenimiento
- **ALWAYS** tipografía serif para headings (Georgia, Playfair Display) + sans para body
- **ALWAYS** incluir número de colegiatura del abogado
- **PREFER** formulario sobre WhatsApp para mantener registro profesional

---

## 7. Inmobiliaria / Bienes Raíces

### Secciones (en orden)

1. **Hero** — foto de propiedad destacada + buscador de propiedades
2. **Propiedades destacadas** — grid de cards con foto, ubicación, precio, m², habitaciones
3. **Por qué nosotros** — años de experiencia, propiedades vendidas, satisfacción cliente
4. **Proceso de compra** — 5 pasos desde búsqueda hasta escritura
5. **Testimonios** — clientes que ya compraron
6. **Zonas** — mapa interactivo o cards por distrito/zona
7. **Contacto** — formulario con campo de presupuesto

### Card de propiedad

```html
<article class="property-card">
  <a href="/propiedades/miraflores-3hab" class="property-img-link">
    <picture>
      <source srcset="depa-miraflores.webp" type="image/webp">
      <img
        src="depa-miraflores.jpg"
        alt="Departamento de 3 habitaciones en Miraflores con vista al mar"
        width="400"
        height="267"
        loading="lazy"
      >
    </picture>
    <span class="property-badge">Nuevo</span>
  </a>
  <div class="property-info">
    <p class="property-location">
      <svg aria-hidden="true"><!-- pin icon --></svg>
      Miraflores, Lima
    </p>
    <h3 class="property-title">Departamento vista al mar</h3>
    <div class="property-specs">
      <span title="3 habitaciones">🛏 3</span>
      <span title="2 baños">🚿 2</span>
      <span title="85 metros cuadrados">📐 85 m²</span>
    </div>
    <p class="property-price">USD 185,000</p>
    <a href="/propiedades/miraflores-3hab" class="btn-property">Ver propiedad</a>
  </div>
</article>
```

---

## 8. Centro Médico / Clínica General

### Secciones (en orden)

1. **Hero** — foto limpia del centro, titular de bienestar, "Agenda tu cita"
2. **Especialidades** — grid de 6–8 especialidades (cardiología, pediatría, dermatología, etc.)
3. **Médicos** — grid de doctores con foto, nombre, especialidad, colegiatura
4. **Servicios de apoyo** — laboratorio, rayos X, farmacia, etc.
5. **¿Por qué elegirnos?** — equipamiento, convenios de salud, emergencias 24h
6. **Seguros aceptados** — logos de EPS y seguros
7. **Ubicaciones** — si tienen varias sedes, mapa con cards por sede
8. **Agendar cita** — formulario o enlace a sistema de citas

### Componentes de accesibilidad críticos

```html
<!-- Información de emergencia — siempre visible -->
<div class="emergency-banner" role="alert">
  <strong>Emergencias 24h:</strong>
  <a href="tel:+51999999999" class="emergency-number">+51 999 999 999</a>
</div>

<!-- Card médico con colegiatura -->
<article class="doctor-card">
  <img
    src="dr-garcia.jpg"
    alt="Dr. Carlos García, Cardiólogo"
    width="200"
    height="200"
    loading="lazy"
  >
  <h3 class="doctor-name">Dr. Carlos García</h3>
  <p class="doctor-specialty">Cardiología Intervencionista</p>
  <p class="doctor-credentials">CMP 12345 · RNE 6789</p>
  <a href="/doctores/carlos-garcia" class="doctor-link">Ver perfil</a>
</article>
```

---

## 9. Educación / Instituto / Academia

### Secciones (en orden)

1. **Hero** — foto de ambiente de aprendizaje, headline de transformación de carrera
2. **Programas / Cursos** — grid de cards con foto, nombre, duración, modalidad, precio
3. **¿Para quién es?** — perfil del estudiante ideal (1–3 bullets específicos)
4. **Metodología** — cómo enseñan (online/presencial, proyectos, mentoring)
5. **Instructores** — perfil con foto, industria de donde vienen
6. **Egresados / Empleabilidad** — empresas donde trabajan, estadísticas
7. **Testimonios** — de egresados con nombre, empresa actual, cargo
8. **Inscripción / Próxima cohorte** — fecha inicio, cupos restantes, formulario

### Componentes especiales

```html
<!-- Card de curso con urgencia -->
<article class="course-card">
  <div class="course-img-wrapper">
    <picture>
      <source srcset="curso-ux.webp" type="image/webp">
      <img src="curso-ux.jpg" alt="Curso de UX Design" width="400" height="225" loading="lazy">
    </picture>
    <span class="course-tag">Modalidad: Online</span>
  </div>
  <div class="course-body">
    <h3 class="course-title">UX Design Profesional</h3>
    <div class="course-meta">
      <span>⏱ 12 semanas</span>
      <span>📅 Inicia 3 Mar</span>
      <span class="course-seats">⚠ 8 cupos restantes</span>
    </div>
    <p class="course-desc">De cero a portafolio completo, con proyectos reales.</p>
    <div class="course-footer">
      <p class="course-price">S/ 1,200 <span class="course-price-full">~~S/ 1,800~~</span></p>
      <a href="/inscripcion/ux-design" class="btn-enroll">Inscribirme</a>
    </div>
  </div>
</article>
```

---

## 10. Hotel / Hospedaje / Airbnb

### Secciones (en orden)

1. **Hero** — foto del lugar con mayor impacto (piscina, vista, habitación), botón "Reservar"
2. **Galería** — 12+ fotos organizadas por área (habitaciones, baños, común, vistas)
3. **Habitaciones** — cards de cada tipo con fotos, nombre, capacidad, precio por noche
4. **Amenidades** — grid de íconos con WiFi, desayuno, piscina, parking, etc.
5. **Ubicación y alrededores** — mapa + qué hay cerca (distancias a puntos de interés)
6. **Reseñas** — estrellas promedio + 3–5 reseñas de Booking/Airbnb
7. **Reservas** — widget de Booking o formulario directo

### Card de habitación

```html
<article class="room-card">
  <div class="room-gallery">
    <!-- Slider de fotos de la habitación -->
  </div>
  <div class="room-info">
    <h3 class="room-name">Suite Deluxe con Vista al Mar</h3>
    <div class="room-specs">
      <span title="Capacidad máxima">👥 2 personas</span>
      <span title="Tamaño">📐 35 m²</span>
      <span title="Cama">🛏 King Size</span>
    </div>
    <ul class="room-amenities">
      <li>Vista panorámica al océano</li>
      <li>Baño privado con bañera</li>
      <li>Aire acondicionado</li>
    </ul>
    <div class="room-booking">
      <p class="room-price">Desde <strong>USD 85</strong>/noche</p>
      <a href="/reservar?room=suite-deluxe" class="btn-reserve">Reservar</a>
    </div>
  </div>
</article>
```

---

## Patrones Transversales (aplican a todas las industrias)

### Horarios de atención (universal)

```css
.hours-table {
  width: 100%;
  border-collapse: collapse;
  font-size: 0.9375rem;
}

.hours-table th,
.hours-table td {
  padding: 12px 0;
  border-bottom: 0.5px solid rgba(0, 0, 0, 0.08);
  text-align: left;
}

.hours-table th {
  font-weight: 500;
  color: #1d1d1f;
  width: 45%;
}

.hours-table td { color: #6e6e73; }

/* Día actual destacado */
.hours-table tr.today th,
.hours-table tr.today td {
  color: #0071e3;
  font-weight: 500;
}
```

### Mapa de Google embebido (accesible)

```html
<div class="map-container" role="region" aria-label="Mapa de ubicación">
  <iframe
    src="https://www.google.com/maps/embed?pb=..."
    width="100%"
    height="400"
    style="border:0; border-radius: 16px;"
    allowfullscreen=""
    loading="lazy"
    referrerpolicy="no-referrer-when-downgrade"
    title="Ubicación de [Empresa] en [Ciudad]"
  ></iframe>
</div>

<!-- Siempre ofrecer alternativa de texto para accesibilidad -->
<p class="map-address">
  <strong>Dirección:</strong> Av. Principal 123, Lima.
  <a href="https://goo.gl/maps/xyz" target="_blank" rel="noopener">
    Ver en Google Maps →
  </a>
</p>
```

### Botón de llamada (mobile-first)

```html
<!-- En mobile, el botón de llamada es gold -->
<a href="tel:+51999999999" class="btn-call" aria-label="Llamar a Empresa">
  <svg aria-hidden="true"><!-- phone icon --></svg>
  <span>Llamar ahora</span>
</a>

<!-- Solo mostrar en mobile — en desktop mostrar el número textual -->
<style>
.btn-call { display: inline-flex; }
@media (min-width: 768px) { .btn-call { display: none; } }
.phone-text { display: none; }
@media (min-width: 768px) { .phone-text { display: inline; } }
</style>
```

### Logos de clientes / partners (carousel en mobile)

```css
.clients-row {
  display: flex;
  gap: 40px;
  align-items: center;
  flex-wrap: wrap;
  justify-content: center;
}

.client-logo {
  height: 32px;
  width: auto;
  opacity: 0.5;
  filter: grayscale(100%);
  transition: opacity 0.2s, filter 0.2s;
}

.client-logo:hover {
  opacity: 1;
  filter: none;
}

@media (min-width: 768px) {
  .clients-row {
    flex-wrap: nowrap;
    justify-content: space-between;
  }
}
```

---

## Anti-Patterns por Industria

| Industria | Anti-Pattern | Fix |
|---|---|---|
| Restaurante | Menú como PDF | HTML con secciones buscables |
| Odontología | Fotos antes/después sin contexto | Incluir tratamiento y duración |
| Consultora | Describir el servicio, no el resultado | "Ahorra 40 horas/mes", no "Ofrecemos consultoría" |
| Gym | Precio solo al final | Mostrar planes desde la sección 2–3 |
| Abogados | Lenguaje jurídico en el hero | Hablar como el cliente, no como abogado |
| Salón | Solo fotos del lugar | Mostrar el trabajo (cortes, uñas, resultados) |
| Clínica | Médicos sin colegiatura | Siempre incluir CMP |
| Academia | "Somos los mejores" | Datos: % empleabilidad, empresas empleadoras |
| Hotel | Una sola foto del cuarto | Galería de 5+ fotos por habitación |

---

## Checklist por Industria

Antes de entregar cada sitio, verificar:

- [ ] ✅ Foto del hero es de la mayor calidad disponible (no stock genérico)
- [ ] ✅ Toda la información del negocio está correcta (horarios, teléfono, dirección)
- [ ] ✅ CTA principal está visible en la primera pantalla sin scroll
- [ ] ✅ Botón de WhatsApp o llamada visible en mobile
- [ ] ✅ Horarios de atención presentes
- [ ] ✅ Dirección física linkea a Google Maps
- [ ] ✅ Formulario de contacto funciona y tiene mensaje de confirmación
- [ ] ✅ Schema.org LocalBusiness incluido en el `<head>`
- [ ] ✅ Todos los textos son del negocio real (no placeholder Lorem Ipsum)
- [ ] ✅ Imágenes tienen alt text descriptivo y específico
