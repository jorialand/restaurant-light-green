# V1 — Referencia visual primera versión (Emergent.sh)

**URL original:** https://vanilla-menu-hub.preview.emergentagent.com/
**Fecha de captura:** 2026-04-05
**Generado con:** Emergent.sh (agentic web app builder)

> Para captura visual completa: abrir la URL en el navegador → Ctrl+S → guardar como
> `docs/v1-emergent-snapshot.html` en esta misma carpeta.

---

## Estructura de la página

| Zona | Descripción |
|---|---|
| Header fijo (76px) | "LIGHT GREEN" en dorado + "Bar & Grill" subtítulo |
| Nav fijo (58px) | 3 tabs: 🥩 Carnes · 🍺 Bebidas · 🍽️ Platos |
| Main (scrollable) | Cards de menú con foto, nombre y precio |
| Footer | "Light Green Bar & Grill, Golf del Sur, Tenerife" |
| Botón WhatsApp (fijo, abajo-izquierda) | Circular, 56px, gradiente verde, enlaza a +34633304131 |
| Botón volver-arriba (fijo, abajo-derecha) | Circular, 46px, aparece tras 280px de scroll |

## Paleta de colores

```css
--green-dark: #141f14   /* fondo principal */
--green-mid:  #2b5226   /* hover */
--gold:       #c9a84c   /* bordes, acento */
--gold-light: #e8c97a   /* títulos, texto activo */
--cream:      #f4efe5   /* texto normal */
```

## Contenido del menú

### 🥩 Carnes (tab por defecto)
| Plato | Precio |
|---|---|
| Wagyu Japonés a la Parrilla | 35€ |
| Chuletón cortada con hueso | 32.50€ |
| Costata cortada con hueso | 29.50€ |
| Solomillo a la Parrilla | 22€ |
| Pulpo a la Parrilla | 20€ |
| Cordero a la Parrilla | 18€ |
| Porchetta de Cerdo | 18€ |
| Cortada de ternera | 18€ |

### 🍺 Bebidas
- Cervezas: Estrella Caña 1.50€, Jarra 3€, Heineken 3€
- Vinos Tintos: Tempranillo, Malbec argentino, Ribera del Duero, Marqués de Cáceres, Protos
- Cocktails Clásicos: Mojito/Margarita/Piña Colada/Daiquiri 8€ · Aperol Spritz/Gin Tonic 7€
- Cocktail Signature: "Light Green" Aloe Vodka 7€
- Refrescos: Agua 2.50€, Coca-Cola/Fanta/Sprite 2.80€, Zumos 3€

### 🍽️ Platos
| Plato | Precio |
|---|---|
| Desayuno con bebida incluida | 9€ |
| Pasta con costillas mixtas | 14€ |
| Arroz basmati con pollo a la parrilla | 12€ |
| Huevos rellenos | 5.50€ |
| Tapa de mortadela | 6.50€ |
| Pan con manteca y jamón | 6€ |
| Alioli con aceitunas | 4€ |
| Chicharrones con guacamole | 7€ |
| Tortilla de papa con ensalada | 9€ |
| Mich con Mustaza | 9€ |
| Postre de frutas, chocolate y helado | 8€ |

## Datos de contacto encontrados en el código

- **WhatsApp:** +34633304131
- **Google Maps:** https://maps.app.goo.gl/USXSJQAjL3BvbmFz5

## Diferencias con nuestra versión actual

| Elemento | V1 Emergent | Nuestra versión |
|---|---|---|
| Botón WhatsApp | Sí, fijo abajo-izquierda, circular | Comentado (pendiente activar) |
| Botón Google Maps | No | Sí, en contact bar |
| Botón Instagram | No | Comentado (pendiente) |
| Botón Reservar | No | Comentado (pendiente) |
| Contact bar | No (botones sueltos) | Sí, barra fija unificada |
| Archivos de Emergent | Sí (frontend/, backend/, etc.) | Eliminados |
