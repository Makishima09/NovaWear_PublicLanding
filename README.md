# NOVA WEAR — Landing Page Template

Landing page profesional para tienda de ropa con presencia física y online. Construida con HTML, CSS y JavaScript vanilla — sin frameworks, sin dependencias, lista para personalizar.

**Demo en vivo:** [NovaWear Public Landing](https://makishima09.github.io/NovaWear_PublicLanding/)

---

## Estructura del proyecto

```
nova-wear/
├── index.html              ← Página principal (toda la landing)
├── css/
│   └── styles.css          ← Todos los estilos
├── js/
│   └── main.js             ← Navbar + menú móvil + animaciones
├── img/
│   ├── camisa-hawaiana.png ← Favicon + icono navbar
│   ├── whatsapp.png        ← Icono WhatsApp del footer
│   ├── productoFrontal.png ← Producto estrella, vista frontal
│   ├── productoEspalda.png ← Producto estrella, vista trasera
│   └── imagenTiendaa.png   ← Interior de la tienda (sección About)
├── PLAN.md                 ← Historial de decisiones del proyecto
├── COPY.md                 ← Todos los textos de la marca
└── WIREFRAME.html          ← Esquema visual de la estructura
```

---

## Cómo ejecutarlo localmente

1. Descarga o clona el repositorio:
   ```bash
   git clone https://github.com/Makishima09/NovaWear_PublicLanding.git
   ```
2. Abre la carpeta en **VS Code**.
3. Instala la extensión **Live Server** (si no la tienes).
4. Haz clic derecho en `index.html` → **Open with Live Server**.
5. El sitio se abre en `http://127.0.0.1:5500` y se actualiza en tiempo real al guardar.

> Sin Live Server, también puedes abrir `index.html` directamente en el navegador — funciona igual salvo el hot-reload.

---

## Publicar en GitHub Pages (gratis)

1. Sube el proyecto a un repositorio público en GitHub.
2. Ve a **Settings → Pages**.
3. En *Source*, selecciona la rama `main` y la carpeta `/ (root)`.
4. Guarda. En 1-2 minutos tendrás una URL pública del tipo `https://tu-usuario.github.io/tu-repo/`.

---

## Guía de personalización

### 1. Colores y tipografía

Abre `css/styles.css` y edita las variables al inicio del archivo (bloque `:root`):

```css
:root {
  --c-bg:     #F5F5F0;  /* Fondo principal — cámbialo por cualquier color claro */
  --c-dark:   #0A0A0A;  /* Color oscuro — fondo del hero, store, footer */
  --c-accent: #00FF87;  /* Color acento — botones, iconos, resaltes */
}
```

Con solo cambiar estos tres valores transformas toda la paleta del sitio.

### 2. Tipografía

La fuente actual es **Gelasio** (Google Fonts). Para cambiarla:

**Paso 1** — En `index.html`, reemplaza el `<link>` de Google Fonts:
```html
<!-- Busca esta línea y cambia la URL -->
<link href="https://fonts.googleapis.com/css2?family=Gelasio:ital,wght@0,400;0,500;0,600;0,700;1,400&display=swap" rel="stylesheet">
```

**Paso 2** — En `css/styles.css`, actualiza las variables:
```css
--f-title: 'TuNuevaTipografía', serif;
--f-body:  'TuNuevaTipografía', serif;
```

Fuentes urbanas recomendadas en Google Fonts: `Bebas Neue`, `Oswald`, `Anton`, `Barlow Condensed`.

### 3. Nombre de marca y textos

Todos los textos están en `index.html`. Las partes que normalmente hay que cambiar:

| Qué cambiar | Dónde buscarlo en index.html |
|---|---|
| Nombre "NOVA WEAR" | Busca `NOVA WEAR` (aparece en navbar, footer y `<title>`) |
| Tagline del hero | `VISTE AL NIVEL QUE MERECES.` |
| Subtítulo del hero | `Calidad premium que se nota desde el primer tacto.` |
| Tag de colección | `Bomber Collection 2026` |
| Textos de About | Los dos párrafos dentro de `.about__body` |
| Estadísticas | Los tres bloques `.stat` (número + etiqueta) |
| Año de fundación | El badge `EST.<br>2020` |
| Copyright | `© 2026 NOVA WEAR. Todos los derechos reservados.` |

### 4. Imágenes

Sustituye los archivos en la carpeta `img/` manteniendo los mismos nombres, o cambia la ruta `src` en el HTML:

| Imagen | Usado en | Recomendación |
|---|---|---|
| `camisa-hawaiana.png` | Favicon + navbar | Logo de tu marca (cuadrado, fondo transparente) |
| `productoFrontal.png` | Sección Producto | Foto del producto, fondo blanco o claro |
| `productoEspalda.png` | Sección Producto | Segunda vista del producto |
| `imagenTiendaa.png` | Sección About | Foto de tu tienda, equipo o marca |
| `whatsapp.png` | Footer | Icono de cualquier red social extra |

> Para el favicon y el icono del navbar se recomienda una imagen cuadrada de al menos 64×64 px con fondo transparente (formato PNG).

### 5. Datos de contacto de la tienda

En `index.html`, busca la sección `<section id="store">` y reemplaza los datos mock:

```html
<!-- DIRECCIÓN -->
<address>
  Calle Gran Vía 42, Local 3<br>
  28013 Madrid, España
</address>

<!-- HORARIO -->
<p>
  Lun – Vie: 10:00 – 21:00<br>
  Sábado: 10:00 – 22:00<br>
  Domingo: 11:00 – 20:00
</p>

<!-- TELÉFONO -->
<a href="tel:+34911234567">+34 911 234 567</a>

<!-- EMAIL -->
<a href="mailto:hola@novawear.com">hola@novawear.com</a>
```

### 6. Mapa de Google Maps

Busca el `<iframe>` dentro de `<div class="store__map">` y reemplaza el atributo `src` con el embed de tu dirección real:

1. Ve a [maps.google.com](https://maps.google.com) y busca tu dirección.
2. Haz clic en **Compartir → Insertar un mapa**.
3. Copia el atributo `src` del `<iframe>` que te da Google y pégalo en el HTML.

### 7. Redes sociales

En el `<footer>`, los enlaces de redes sociales apuntan a `#`. Reemplázalos con las URLs reales:

```html
<a href="https://instagram.com/tu-cuenta" aria-label="Instagram" class="social--instagram">
<a href="https://tiktok.com/@tu-cuenta" aria-label="TikTok" class="social--tiktok">
<a href="https://x.com/tu-cuenta" aria-label="X / Twitter" class="social--x">
<a href="https://wa.me/34XXXXXXXXX" aria-label="WhatsApp">
```

Para WhatsApp, el formato del enlace es `https://wa.me/` seguido del número sin espacios ni `+` (ej: `https://wa.me/34911234567`).

### 8. Secciones (añadir o eliminar)

Cada sección es un bloque independiente en `index.html`. Para **eliminar** una sección, borra el bloque completo desde `<section id="...">` hasta su `</section>` de cierre. Para **añadir** una nueva, copia la estructura de cualquier sección existente como punto de partida.

Si eliminas una sección, recuerda también quitar su enlace en el navbar:
```html
<nav class="navbar__nav">
  <a href="#hero">Inicio</a>
  <a href="#about">Nosotros</a>   ← elimina esta línea si borras #about
  <a href="#store">Tienda</a>
  <a href="#contact">Contacto</a>
</nav>
```

---

## Tecnologías usadas

| Tecnología | Para qué |
|---|---|
| HTML5 semántico | Estructura de la página |
| CSS3 (variables, Flexbox, Grid, clamp) | Diseño y responsividad |
| JavaScript vanilla | Navbar scroll, menú móvil, animaciones de entrada |
| Google Fonts CDN | Tipografía Gelasio |
| Font Awesome 6 CDN | Iconos (mapa, reloj, teléfono, email, redes sociales) |
| Intersection Observer API | Animaciones al hacer scroll |

---

## Créditos

Diseñado y construido como plantilla de landing page para tiendas de ropa urbana.  
Imágenes de producto: propias de NOVA WEAR.
