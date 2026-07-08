# ROE Colombia — demo narrado

Presentación auto-reproducible del **Reporte Obligatorio de Emisiones (ROE)** de Colombia
(Ministerio de Ambiente y Desarrollo Sostenible), contada en primera persona por una
gerente ambiental que reporta las emisiones de su empresa en el portal
[home-colombia.eregistrations.org](https://home-colombia.eregistrations.org/).

**▶ Ver en vivo (español): https://nelsonadpa.github.io/roe-colombia-demo/**
**▶ Watch live (English): https://nelsonadpa.github.io/roe-colombia-demo/en.html**

Ambas versiones llevan un botón ES/EN arriba a la derecha para cambiar de idioma.

Sigue el patrón del demo [Easy Accounts Uganda](https://github.com/unctad-ai/uganda-demo):
un HTML estático, un clip de narración por slide, y el audio es el reloj — cada slide
dura exactamente lo que dura su narración y avanza al terminar.

## La historia (11 slides)

1. Portada — de las hojas de cálculo a un portal en línea
2. Qué es el ROE — 2025 en modo prueba, obligatorio desde 2026
3. Quién debe reportar — umbral de 11.000 tCO₂eq/año
4. Un solo portal oficial (Gov.co / Ministerio de Ambiente)
5. Ingreso — correo, NIT o cuenta Gov.co
6. Mi cuenta — historial de reportes con vigencia y estado
7. El formulario paso a paso — vigencia y tipo de reporte
8. Fuentes de emisión — menús en cascada hasta la fuente exacta
9. El sistema calcula — dato de actividad + factores de emisión oficiales
10. Resultado — grid consolidado con las emisiones calculadas (14.520,7 tCO₂eq, supera el umbral)
11. Constancia oficial con código QR de verificación

## Voz

Narración generada con Microsoft Edge neural TTS, un MP3 por slide:

- **Español:** voz colombiana **`es-CO-SalomeNeural`** (`assets/audio/s0..s10.mp3`)
- **English:** voz **`en-US-AvaNeural`** (`assets/audio/en_s0..en_s10.mp3`)

Para regenerar un clip:

```bash
uvx edge-tts --voice es-CO-SalomeNeural --rate "+8%" \
  --text "..." --write-media assets/audio/sN.mp3
```

## Pantallas

Las imágenes en `assets/shots/` son capturas reales del portal
`home-colombia.eregistrations.org` y del servicio "Reporte obligatorio de emisiones"
del ambiente de prueba de Colombia (julio 2026). Las cifras que se ven son datos de prueba.

## Mecánica

- HTML/CSS/JS puro, sin build. Un solo `index.html`.
- Cada `<section class="slide">` lleva `data-audio`; al terminar el audio avanza (`onended`).
- Controles: ⏮ ← ▶/⏸ → · flechas del teclado · espacio para pausar.
- Publicado con GitHub Pages (branch `main`, raíz).

---
Iniciativa del Ministerio de Ambiente y Desarrollo Sostenible de Colombia, con el apoyo
del Reino de los Países Bajos y de **ONU Comercio y Desarrollo (UNCTAD)** — programa eRegistrations.
