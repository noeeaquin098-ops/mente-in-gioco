# Guía de Marca — Mente in Gioco™
**Fuente verificada: `Mente in Gioco BRANDING.txt` (archivo original adjunto en `archivos/BRANDING-ORIGINAL.txt`)**
**Todas las reglas aquí son ✅ APROBADAS salvo indicación contraria.**

---

## 1. CONCEPTO RECTOR

**"Il tabellone dei progressi"** — El tablero de los progresos.

Imagen mental: un juego de mesa sobre la mesa de la cocina. El producto no es un ejercicio escolar ni una app educativa. Es un juego que se juega en familia, con piezas físicas, en la mesa real de casa.

**De qué se aparta explícitamente (prohibido replicar):**
- Pastel lavado de guardería (verde menta, lila bebé, palo de rosa)
- Tarjetas blancas con íconos lineales (el default de los infoproductos de bienestar)
- Neón de apps infantiles
- Cerebro con cara — NeuroKids y Neurocarte ya lo tienen; NO diferencia, iguala

---

## 2. PALETA DE COLORES

| Token CSS | Hex | Uso |
|-----------|-----|-----|
| `--cream` | `#FBF7EE` | Fondo principal — pergamino cálido |
| `--cream-alt` | `#F3EADA` | Fondo alternativo, fondos de sección |
| `--tablero` | `#17494A` | Verde oscuro — color ancla de marca |
| `--mandarina` | `#E8692F` | Naranja — acento E1 / sección Focus |
| `--dorado` | `#C9A227` | Dorado — acento secundario |
| `--amarillo` | `#F2B33D` | Amarillo — acento E2 / sección Emozioni |
| `--verde` | `#5C9E5A` | Verde claro — acento E3 / sección Piano Guida |

**Progresión por sección (obligatoria):**
- E1 Focus → color `--mandarina`
- E2 Emozioni → color `--amarillo`
- E3 Piano Guida → color `--verde`

---

## 3. TIPOGRAFÍA

| Familia | Peso | Uso |
|---------|------|-----|
| Baloo 2 | 700, 800 | Titulares, H1, H2 — calidez y redondez infantil sin ser de guardería |
| Nunito | 400, 600, 700 | Cuerpo de texto, descripciones, botones |

Fuente: Google Fonts (cargadas en la landing actual).

---

## 4. PERSONAJE: GINO

**Descripción:** Peón de madera de juego de mesa. Sin cara humana, sin expresión. Forma simple de peón clásico, textura de madera visible.

**No es:** un cerebro con cara, un niño dibujado, un personaje genérico de app educativa.

**Implementación actual:** generado por JavaScript como SVG inline en la landing. Aparece exactamente 3 veces:
- Logo del header: 32×51 px
- Sección hero: 80×128 px  
- CTA final: 64×102 px

**Por qué Gino importa:** Es el único elemento del nicho sin cerebro con cara. KidooLabs tiene un logo con ojitos pero no un personaje con nombre. Gino es diferenciador real.

---

## 5. ELEMENTOS GRÁFICOS

### Separadores de casilla
SVG con trayecto punteado y círculos numerados entre secciones principales. Representan el avance en el tablero de 30 días. Hay 3 casillas en la landing actual.

### Tablero de 30 días (sección #firma)
Cuadrícula HTML de 30 casillas numeradas, coloreadas por tramo (mandarina/amarillo/verde según la progresión). Es el elemento más diferenciador del producto y el único que ningún competidor puede mostrar.

### Imágenes de fondo de sección
Texturas sutiles que refuerzan el concepto de tablero / papel / madera. Nunca fondos lisos blancos.

---

## 6. CONCEPTO DE IMAGEN (prompts base verificados desde BRANDING.txt)

### Mockups de producto (ratio 1:1)
```
Square photograph, oak table, wooden pencils, wooden pawn, 
daylight from upper-left, no screens, scattered sheets of paper, 
background #FBF7EE, photorealistic, warm light, depth of field
```

### Vistazo de actividades (ratio 4:5)
```
Flat A4 sheet on cream background, crayon illustration style, 
palette #E8692F/#F2B33D/#5C9E5A/#17494A on #FBF7EE,
[descripción de la actividad específica], 
no text inside image, clean margins
```

**⚠️ Advertencia crítica:** Las 15 imágenes AI existentes son MOCKUPS CONCEPTUALES, no capturas del PDF real (que no existe aún). Las imágenes de vistazo muestran actividades conceptuales en estilo crayón — el PDF real deberá coincidir con ese nivel visual.

---

## 7. TONO DE COMUNICACIÓN

**Registro:** Italiano cotidiano, cálido, directo. Ni académico ni excesivamente informal.

**Voz del padre (avatar):** Se siente culpable, no incompetente. Busca una solución concreta, no educación ni teoría.

**Evitar siempre:**
- Lenguaje clínico ("estimulación cognitiva", "neuroplasticidad")
- Tono de coach motivacional
- Frases genéricas de autoayuda
- Comparar al niño con otros de forma negativa

**Evitar por decisión de operación:**
- "real/reales" en copy — suena a generado por IA
- Resultados sin condición en nichos de salud/educación
- Urgencia sobre el precio (la urgencia va sobre los bonos, nunca sobre el precio)

---

## 8. RESTRICCIONES HEREDADAS DEL ANÁLISIS DE COMPETENCIA

Elementos que los competidores usan y que Mente in Gioco NO debe replicar:

| Elemento | Por qué no replicar |
|---------|---------------------|
| "Solo hoy" sobre el precio | Artificial; si el precio no cambia, se desmiente sola |
| Nota social inventada ("X familias") | No hay ventas aún — toda cifra es ficticia |
| Testimonios sin permiso real | Riesgo ético y de confianza |
| Cerebro con cara como mascota | Default del nicho; no diferencia |
| Garantía corta para método largo | 7 días de garantía para un método de 30 días es incongruente |
