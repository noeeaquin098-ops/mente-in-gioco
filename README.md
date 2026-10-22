# Mente in Gioco™

PDF imprimibile per allenare l'attenzione dei bambini, senza schermi. Mercato: Italia.

**Estado del proyecto:** Landing técnicamente completa · PDFs del producto no producidos · Checkout pendiente de configurar · Sin ads activos.

---

## Estructura del repositorio

```
docs/                        ← Documentación del proyecto
  TRASPASO-MENTE-IN-GIOCO.md ← Documento maestro de traspaso (fuente de verdad)
  BRANDING.md                ← Guía de marca aprobada (paleta, tipografía, Gino)
  ESTADO-TECNICO.md          ← Estado técnico de la landing + pendientes
  INVENTARIO-PRODUCTO.md     ← Producto, precios, entregables, garantía
  REFERENCIAS-Y-ANALISIS.md  ← Análisis de competidores
  CORE-OFFER-ORIGINAL.txt    ← Fuente original del producto (texto plano)
  BRANDING-ORIGINAL.txt      ← Brandbook original (texto plano)

landing/
  index.html                 ← Landing completa (HTML estático, 1229 líneas)
  img/                       ← 15 imágenes PNG (mockups conceptuales AI)

assets/
  producto/                  ← PDFs del producto cuando existan (vacío)
  mockups/                   ← Mockups adicionales (vacío)
  ilustraciones/             ← Ilustraciones adicionales (vacío)
```

---

## Pendientes críticos antes de activar ventas

1. **Checkout** — reemplazar los 3 `[[URL_CHECKOUT]]` en `landing/index.html` con la URL real de Impultienda
2. **Testimonios** — la sección `#testimonianze` contiene testimonios ficticios; reemplazar o eliminar
3. **Píxel Meta Ads** — no instalado en el `<head>` de `landing/index.html`

---

## Notas importantes

- Las imágenes en `landing/img/` son **mockups conceptuales generados con IA**, no capturas del producto real. El PDF del producto no existe todavía.
- Los 6 PDFs del producto (E1, E2, E3, B1, B2, B3) se producirán tras las primeras 3 ventas.
- El HTML no contiene claves ni datos sensibles.

---

## División de trabajo

| Rol | Responsabilidad |
|-----|----------------|
| ChatGPT | Dirección creativa, decisiones de diseño, UX, estrategia de conversión, revisión de landing |
| Claude Code | Contexto del producto, implementación técnica, archivos, soporte de ejecución |
| Noemí | Aprobaciones, decisiones de negocio, activación de ads |

---

## Precio y comercial

- Precio de lanzamiento: **15,90 €** (pago único, acceso de por vida)
- Precio ancla: 44,50 € (−64%)
- Garantía: "Primi Passi" — 15 días condicionada al uso real del Piano Guida
- Pasarela: Impultienda (pendiente de configurar)
