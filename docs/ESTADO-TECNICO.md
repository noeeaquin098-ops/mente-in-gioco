# Estado Técnico de la Landing — Mente in Gioco™
**Verificado el 22/10/2026 contra el archivo real `landing/index.html`**

---

## 1. TECNOLOGÍA Y ESTRUCTURA

| Atributo | Valor |
|----------|-------|
| Tipo | HTML estático (un solo archivo) |
| Framework | Ninguno — HTML + CSS + JS vanilla |
| Build step | No requiere — se abre directamente en browser |
| Dependencias externas | Google Fonts (Baloo 2 + Nunito) vía CDN |
| Servidor requerido | No — funciona como archivo local |
| Responsive | Sí — mobile-first con media queries |
| Total de líneas | 1.229 líneas |

---

## 2. ARCHIVOS PRINCIPALES

| Archivo | Ruta | Estado |
|---------|------|--------|
| `index.html` | `landing/index.html` | ✅ Completo — 1.229 líneas |
| Imágenes (15 PNG) | `landing/img/*.png` | ✅ Completo — 15/15 presentes |
| CSS | Inline dentro de `index.html` | ✅ Completo |
| JavaScript | Inline dentro de `index.html` | ✅ Completo (Gino SVG + timer) |

**No hay archivos CSS o JS externos.** Todo está en `index.html`.

---

## 3. SECCIONES IMPLEMENTADAS (en orden)

| ID de sección | Nombre | Estado |
|---------------|--------|--------|
| `#header` | Logo + navegación | ✅ |
| `#hero` | H1, subtítulo, CTA, imagen hero | ✅ |
| casilla-1 | Separador SVG numerado | ✅ |
| `#dolori` | 4 dolores del avatar | ✅ |
| `#benefici` | 6 beneficios | ✅ |
| `#soluzione` | Sección solución + imagen | ✅ |
| `#firma` | Tablero 30 casillas (mecanismo visual) | ✅ |
| `#passi` | Cómo funciona en 3 pasos | ✅ |
| casilla-2 | Separador SVG numerado | ✅ |
| `#entregables` | E1, E2, E3 con imagen + descripción | ✅ |
| `#vistazo` | 6 imágenes de vistazo del contenido | ✅ |
| `#bonos` | B1, B2, B3 con timer de 15 minutos | ✅ |
| `#testimonianze` | 4 testimonios WhatsApp-style | ⚠️ FICTICIOS (ver §5) |
| `#vg-oferta` | Stack de valor + precio + botón compra | ✅ |
| `#reviews` | Reseñas de 5 estrellas | ⚠️ FICTICIAS (ver §5) |
| casilla-3 | Separador SVG numerado | ✅ |
| `#garanzia` | Garantía "Primi Passi" 15 días | ✅ |
| `#faq` | 6 preguntas frecuentes | ✅ |
| `#cta-finale` | CTA final con Gino | ✅ |
| `#footer` | Footer con datos legales | ✅ |
| `#float-cta` | Botón flotante de compra | ✅ |

---

## 4. FUNCIONALIDADES OPERATIVAS

### Timer de 15 minutos (bonos)
- Implementado con `sessionStorage`
- Clave: `mente_in_gioco_it_deadline`
- Comportamiento: cuenta 15 minutos desde la primera visita. La copia dice que si pasa el tiempo, los bonos desaparecen (no el precio).
- **Estado: ✅ Funcional** — el timer se inicializa correctamente.
- **Nota de coherencia:** La urgencia está sobre los bonos, no sobre el precio. Es intencionalmente honesto — diferenciador frente a competidores que usan "solo hoy" sobre el precio.

### Gino (mascota SVG)
- Generado por JavaScript como SVG inline en 3 tamaños
- No es una imagen externa — es código JS que dibuja el peón de madera
- **Estado: ✅ Funcional**

### Formulario / checkout
- **⛔ NO FUNCIONAL** — los 3 botones de compra apuntan al placeholder `[[URL_CHECKOUT]]`
- La landing no puede vender todavía

---

## 5. DEFECTOS CONOCIDOS Y PENDIENTES CRÍTICOS

### ⛔ BLOQUEANTE 1 — URL de checkout no configurada
- **Dónde:** líneas 1011, 1115 y 1148 de `index.html`
- **Valor actual:** `[[URL_CHECKOUT]]` (texto literal, no URL)
- **Qué necesita:** URL real de Impultienda una vez configurado el checkout
- **Impacto:** La landing no puede generar ninguna venta hasta que se resuelva

### ⛔ BLOQUEANTE 2 — Testimonios ficticios
- **Dónde:** sección `#testimonianze`
- **Contenido actual:** 4 testimonios inventados — Valentina R., Marco T., Chiara M., Sara P.
- **Qué necesita:** Testimonios reales con permiso, o eliminar la sección hasta tenerlos
- **Impacto:** Riesgo ético y de credibilidad si se activa tráfico de pago

### ⛔ BLOQUEANTE 3 — Píxel de Meta Ads no instalado
- **Dónde:** `<head>` del HTML — no existe ningún código de píxel
- **Qué necesita:** Código del píxel de Meta Ads (Facebook Pixel) a insertar en el `<head>`
- **Impacto:** Sin píxel no hay datos de campaña y los anuncios no pueden optimizarse hacia Purchase

### ⚠️ PENDIENTE — Verificación mobile 375×812 px
- La landing está diseñada mobile-first pero no se verificó visualmente en viewport 375×812 (iPhone SE / iPhone 12 mini)
- El H1 es largo — puede necesitar ajuste de tamaño de fuente en ese viewport

### ⚠️ PENDIENTE — Reseñas ficticias en `#reviews`
- Las reseñas de 5 estrellas son igual que los testimonios: inventadas
- Mismo tratamiento recomendado: reemplazar o eliminar antes de activar tráfico

---

## 6. IMÁGENES

### Imágenes reales presentes (15 PNG en `landing/img/`)

| Archivo | Ratio | Sección de uso | Estado |
|---------|-------|----------------|--------|
| `hero_169.png` | 16:9 | `#hero` | ✅ Conceptual AI |
| `e1_11.png` | 1:1 | `#entregables` E1 | ✅ Conceptual AI |
| `e2_11.png` | 1:1 | `#entregables` E2 | ✅ Conceptual AI |
| `e3_11.png` | 1:1 | `#entregables` E3 | ✅ Conceptual AI |
| `b1_11.png` | 1:1 | `#bonos` B1 | ✅ Conceptual AI |
| `b2_11.png` | 1:1 | `#bonos` B2 | ✅ Conceptual AI |
| `b3_11.png` | 1:1 | `#bonos` B3 | ✅ Conceptual AI |
| `soluzione_11.png` | 1:1 | `#soluzione` | ✅ Conceptual AI |
| `piano_guida_11.png` | 1:1 | `#firma` | ✅ Conceptual AI |
| `vistazo_01.png` → `vistazo_06.png` | ~4:5 | `#vistazo` | ✅ Conceptual AI |

**⚠️ Todas son mockups conceptuales generados con IA (gpt-image-2 vía APIMART).** No son capturas del PDF real — el PDF aún no existe. Las imágenes de vistazo muestran actividades en estilo crayón que el PDF real deberá coincidir.

### Imágenes faltantes
- Imágenes de testimonios reales: no existen
- Banner de checkout (1738×905 px para Impultienda): no existe

---

## 7. VARIABLES CSS (tokens de marca definidos)

```css
--cream: #FBF7EE
--cream-alt: #F3EADA
--tablero: #17494A
--mandarina: #E8692F
--dorado: #C9A227
--amarillo: #F2B33D
--verde: #5C9E5A
```

Definidas al inicio del bloque `<style>` en `index.html`. Todas las secciones usan estos tokens, no valores hex directos.

---

## 8. LO QUE ESTÁ LISTO PARA REUTILIZAR

- Estructura completa de secciones (orden y jerarquía validados)
- CSS base con variables de marca
- JavaScript del timer de sesión (funciona, solo cambiar la key si se clona para otro producto)
- JavaScript del generador de Gino SVG
- Las 15 imágenes conceptuales (válidas para la landing mientras el PDF no exista)
- El texto de todas las secciones excepto testimonios/reseñas

## 9. LO QUE CONVIENE REVISAR ANTES DE ACTIVAR ADS

1. Verificar el H1 en mobile 375px — puede necesitar `font-size` menor
2. Reemplazar o eliminar `#testimonianze` y `#reviews` (contenido ficticio)
3. Instalar píxel de Meta Ads en `<head>`
4. Reemplazar los 3 `[[URL_CHECKOUT]]` con la URL real de Impultienda
