# CLAUDE.md

This file provides guidance to Claude Code (claude.ai/code) when working with code in this repository.

## Qué es este proyecto

Menú digital QR para **Light Green Bar & Grill** (Golf del Sur, Tenerife). El cliente escanea un QR y accede al menú en su móvil.

Generado inicialmente en Emergent.sh. Migrado a propiedad propia con despliegue en Vercel.

**Repo GitHub:** `https://github.com/jorialand/restaurant-light-green.git`

---

## Arquitectura y stack

**Producto real:** `index.html` — fichero único, vanilla HTML/CSS/JS, sin build step, sin dependencias npm.

| Directorio/fichero | Descripción |
|---|---|
| `index.html` | **El sitio web completo.** Toda la UI, estilos y lógica aquí. |
| `vercel.json` | Configuración de despliegue (cache headers, rewrite catch-all). |
| `frontend/` | Scaffolding React generado por Emergent.sh. **Ignorar.** |
| `backend/` | FastAPI + MongoDB generado por Emergent.sh. **Ignorar.** |
| `memory/`, `test_reports/`, `tests/` | Artefactos de Emergent.sh. **Ignorar.** |

No hay build, no hay `npm install`, no hay servidor. El site es el `index.html`.

---

## Despliegue

**Vercel (producción):**
1. Conectar el repo GitHub `jorialand/restaurant-light-green` en vercel.com.
2. Framework preset: **Other** (no framework).
3. Root directory: `/` (raíz del repo).
4. Vercel sirve `index.html` automáticamente. `vercel.json` ya está configurado.

**Preview local:**
```bash
# Cualquiera de los dos vale:
npx serve .
python -m http.server 8080
```

---

## Diseño y brand

Paleta CSS (variables en `:root`):

| Variable | Valor | Uso |
|---|---|---|
| `--green-dark` | `#141f14` | Fondo principal |
| `--green-mid` | `#2b5226` | Hover, backgrounds secundarios |
| `--gold` | `#c9a84c` | Bordes, labels, acento |
| `--gold-light` | `#e8c97a` | Texto destacado, títulos |
| `--cream` | `#f4efe5` | Texto normal |

Todos los componentes nuevos deben usar estas variables. No introducir colores hardcodeados.

---

## Estructura del HTML

```
<header>          — fijo arriba, altura 76px. Logo + nombre.
<nav #tabBar>     — fijo bajo el header, altura 58px. Tabs de sección.
<main>            — scrollable. padding-top: calc(76+58+14px), padding-bottom: 80px.
  <section #panel-carnes>   — panel activo por defecto
  <section #panel-bebidas>  — oculto hasta click
  <section #panel-platos>   — oculto hasta click
  <footer>        — dentro de main, texto de pie.
</main>
<div .contact-bar>  — fijo abajo, altura 62px. Botones de contacto.
<button .back-to-top> — fijo, bottom: 76px (sobre contact bar).
```

---

## Cómo añadir botones a la contact bar

En `index.html`, localizar `<div class="contact-bar">` y copiar el patrón:

```html
<a
  class="contact-btn"
  href="URL_DESTINO"
  target="_blank"
  rel="noopener noreferrer"
>
  EMOJI Texto
</a>
```

Los botones comentados (WhatsApp, Instagram, Reservar) ya están como plantilla — descomentar y rellenar la URL.

---

## Imágenes del menú

Las imágenes están alojadas en la CDN de Emergent.sh:
```
https://customer-assets.emergentagent.com/job_vanilla-menu-hub/artifacts/
```

**Riesgo:** si Emergent.sh retira esas URLs, las imágenes desaparecen. Tarea pendiente: descargar y realojar en GitHub o Cloudinary.

El comentario al final del `index.html` lista todos los nombres de archivo con su plato y precio.

---

## TODOs del cliente

- [x] Google Maps — URL exacta: https://maps.app.goo.gl/USXSJQAjL3BvbmFz5
- [x] Botón WhatsApp activo — número: +34633304131
- [ ] Descomentar y configurar botón Instagram con handle real.
- [ ] Descargar y realojar las imágenes del menú (fuera de CDN de Emergent.sh).
- [ ] Dominio personalizado en Vercel (ej. `menu.lightgreenbarandgrill.com`).
