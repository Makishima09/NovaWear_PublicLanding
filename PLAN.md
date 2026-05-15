# Plan: Landing Page — NOVA WEAR

## Contexto
Landing page profesional para **NOVA WEAR**, una tienda de ropa con presencia tanto física como online. Estilo **Moderno/Urbano** (bold, vibrante, juvenil). Nivel de experiencia del desarrollador: **principiante en HTML/CSS**. El plan es pedagógico: cada fase produce un resultado visible y funcionando.

---

## Identidad de Marca (Definida)

| Elemento | Valor |
|---|---|
| **Nombre** | NOVA WEAR |
| **Color fondo** | `#F5F5F0` — Blanco hueso |
| **Color acento** | `#00FF87` — Verde neón |
| **Color oscuro** | `#0A0A0A` — Negro profundo |
| **Tipografía** | `Gelasio` (Google Fonts) — títulos y texto |
| **Tagline** | "Moda urbana. Sin reglas." |

---

## Estructura del Proyecto

```
nova-wear/
├── index.html                ← El único HTML de la landing       ✅
├── css/
│   └── styles.css            ← Todos los estilos                 ✅
├── js/
│   └── main.js               ← Navbar scroll + menú móvil        ✅
├── img/
│   ├── camisa-hawaiana.png   ← Favicon + icono del navbar        ✅
│   ├── whatsapp.png          ← Icono WhatsApp del footer         ✅
│   ├── productoFrontal.png   ← Bomber vista frontal              ✅
│   ├── productoEspalda.png   ← Bomber vista trasera              ✅
│   └── imagenTiendaa.png     ← Interior tienda (sección About)   ✅
├── PLAN.md                   ← Este fichero                      ✅
├── COPY.md                   ← Copy y textos de la marca         ✅
└── WIREFRAME.html            ← Esquema estructural visual        ✅
```

**Herramientas recomendadas:**
- Editor: VS Code (gratis)
- Extensión: **Live Server** (para ver cambios en tiempo real)
- Imágenes: [unsplash.com](https://unsplash.com) — busca "streetwear" o "urban fashion"

---

## Fase 1 — Identidad de Marca ✅

Completada. Ver tabla de identidad arriba.

---

## Fase 2 — Estructura del Proyecto ✅

Carpetas creadas: `css/`, `js/`, `img/`.

---

## Fase 3 — Estructura HTML ✅

Secciones de la landing en orden:

```
1. <header>             → Navbar fija: icono + logo + links + botón CTA
2. <section#hero>       → Banner: título enorme + subtítulo + 2 botones
3. <section#producto>   → Producto estrella: bomber frontal + trasera + CTA
4. <section#about>      → Historia: imagen tienda + texto + estadísticas
5. <section#store>      → Tienda física: 4 info-cards + mapa Google (mock)
6. <footer#contact>     → Logo + redes sociales + copyright
```

**Reglas para principiantes:**
- Usar etiquetas semánticas (`<header>`, `<main>`, `<section>`, `<footer>`)
- Cada sección tiene un `id` para navegación con anclas (`#hero`, `#about`, etc.)
- No usar estilos inline — todo va en `styles.css`

---

## Fase 4 — Estilos CSS ✅

### 4.1 — Variables CSS globales
```css
:root {
  --c-bg:     #F5F5F0;   /* Blanco hueso */
  --c-dark:   #0A0A0A;   /* Negro profundo */
  --c-accent: #00FF87;   /* Verde neón */
  --f-title:  'Bebas Neue', sans-serif;
  --f-body:   'Inter', sans-serif;
}
```

### 4.2 — Navbar
- Fija en la parte superior (`position: fixed`)
- Transparente al inicio → fondo oscuro al hacer scroll (con JS)
- Logo a la izquierda, links a la derecha
- Botón "Comprar Online" con color acento

### 4.3 — Hero Section
- Fondo oscuro con rejilla sutil de líneas verdes
- Título enorme con `clamp()` (se adapta a cualquier pantalla)
- Overlay con gradiente radial verde para dar profundidad
- Indicador de scroll animado al fondo

### 4.4 — About Section
- Fondo blanco hueso, dos columnas (imagen | texto)
- Placeholder oscuro donde irá la foto real
- Badge circular "EST. 2020" sobre la imagen
- 3 estadísticas con número grande en Bebas Neue

### 4.5 — Store Section
- Fondo oscuro (contraste con About)
- Grid de 2 columnas: info-cards | mapa iframe
- 4 tarjetas con icono verde + datos mock (dirección, horario, tel, email)
- Mapa de Google Maps embebido (Gran Vía, Madrid — datos ficticios)

### 4.6 — Footer
- Fondo muy oscuro (`#050505`)
- Logo + tagline centrado
- 4 iconos de redes sociales (Instagram, TikTok, X, WhatsApp)
- Copyright 2026

---

## Fase 5 — Responsividad (Mobile-first) ✅

| Breakpoint | Ancho | Cambios principales |
|---|---|---|
| Mobile | < 480px | Botones apilados, stats en 2 columnas |
| Tablet | < 768px | Menú hamburguesa, columnas en stack |
| Desktop | > 1024px | Layout completo de 2 columnas |

**Técnicas usadas:**
- `clamp()` para tipografías fluidas
- Flexbox para alineaciones
- CSS Grid para el layout de store
- `@media` queries para breakpoints

---

## Fase 6 — Detalles Profesionales ✅

- [x] `transition: all 0.3s ease` en todos los elementos interactivos
- [x] `scroll-behavior: smooth` para navegación suave
- [x] Google Fonts cargadas via CDN — tipografía cambiada a `Gelasio`
- [x] Font Awesome para iconos (via CDN)
- [x] Meta tags: `description`, `viewport`
- [x] Filtro CSS en el iframe del mapa para integrarlo visualmente al diseño oscuro
- [x] Animaciones de entrada al scroll con Intersection Observer
- [x] Favicon: `camisa-hawaiana.png`
- [x] Icono de marca en el navbar: `camisa-hawaiana.png`
- [x] Icono WhatsApp custom en el footer: `whatsapp.png`
- [x] Imágenes reales añadidas: bomber frontal, bomber trasera, interior tienda

---

## Fase 7 — Verificación Final ✅

- [x] Se ve bien en móvil (`F12 → toggle device` en Chrome)
- [x] Navbar cambia de color al hacer scroll
- [x] El menú hamburguesa funciona en móvil
- [x] El mapa carga correctamente
- [x] Los iconos de redes sociales aparecen con sus colores de marca
- [x] No hay texto "Lorem ipsum" sin reemplazar
- [x] Las fuentes cargan (Gelasio)
- [x] Botones tienen efecto hover visible

---

## Orden de Implementación Recomendado

```
Día 1 → PLAN.md + COPY.md + WIREFRAME.html + carpetas     ✅ Completado
Día 2 → index.html completo (estructura HTML)              ✅ Completado
Día 3 → styles.css: variables + reset + navbar + hero      ✅ Completado
Día 4 → styles.css: about + store + footer                 ✅ Completado
Día 5 → Responsividad (@media queries) + main.js           ✅ Completado
Día 6 → Fase 6: animaciones, favicon, imágenes reales      ✅ Completado
Día 7 → Fase 7: verificación completa + iconos con color   ✅ Completado
Día 8 → Datos reales de tienda (dirección, tel, email)     ⏳ Pendiente
Día 9 → Deploy en GitHub Pages (opcional, gratis)          ⏳ Pendiente
```

---

## Datos Mock (Tienda Física)

> Estos datos son ficticios y deben reemplazarse con los reales cuando estén disponibles.

| Campo | Valor mock |
|---|---|
| Dirección | Calle Gran Vía 42, Local 3, 28013 Madrid |
| Teléfono | +34 911 234 567 |
| Email | hola@novawear.com |
| Horario L-V | 10:00 – 21:00 |
| Horario Sáb | 10:00 – 22:00 |
| Horario Dom | 11:00 – 20:00 |

---

## Notas

- El mapa usa un `iframe` de Google Maps con una dirección ficticia (Gran Vía, Madrid)
- E-commerce real (carrito, pagos) **no está en el scope** de esta landing
- La sección de producto estrella se añadió durante el desarrollo (no estaba en el plan original)
- Los datos de contacto de la tienda (dirección, tel, email, horario) siguen siendo mock
