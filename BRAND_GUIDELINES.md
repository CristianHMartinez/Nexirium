# Nexírium — Brand Guidelines v1.0

> Documento de identidad visual y sistema de diseño · Mayo 2026 · Uso interno

---

## 1. Misión y valores de marca

**Nexírium** digitaliza micro y pequeñas empresas en Ciudad Juárez con sistemas, apps móviles e inteligencia artificial, bajo un modelo de MVP y módulos que elimina la barrera de inversión inicial.

| Pilar | Qué significa |
|---|---|
| Cercano | Equipo local. Conocemos el negocio del cliente por dentro |
| Accesible | Modelo MVP y módulos: tecnología sin costo inicial elevado |
| Socio, no proveedor | No entregamos y desaparecemos. Crecemos junto con cada cliente |
| Local con visión global | Juárez como base; El Paso, Texas y más allá como destino |
| Técnico pero humano | Tecnología en el idioma del cliente, sin jerga innecesaria |

---

## 2. Logotipo

### Versiones disponibles

| Archivo | Variante | Cuándo usar |
|---|---|---|
| `IMAGOTIPO.svg` | Símbolo + nombre | **Uso preferido** en todos los contextos |
| `LOGOTIPO.svg` | Solo el nombre | Cuando el símbolo ya es reconocible en el contexto |
| `ISOTIPO.svg` | Solo el símbolo | Favicon, app icon, espacios muy reducidos |

### Uso sobre fondos

- **Fondo marino (navy-900 `#070D1A`)** → logo en blanco (`filter: brightness(0) invert(1)`)
- **Fondo claro (neutral-50 `#F7F6F4`)** → logo en marino original (`fill: #001331`)
- **Fondo negro** → logo en blanco o dorado

### Reglas de protección

- **Espacio mínimo**: dejar un margen equivalente a la altura de la «N» del wordmark en todos los lados del logo. Ningún otro elemento gráfico dentro de esa zona.
- **Tamaño mínimo digital**: 120 px de ancho para el imagotipo; 32 px de ancho para el isotipo.
- **Tamaño mínimo impresión**: 30 mm de ancho para el imagotipo.

### Usos incorrectos — nunca hacer esto

- Distorsionar o estirar las proporciones
- Rotar el logotipo
- Cambiar los colores del logo por colores fuera de la paleta
- Aplicar efectos (sombra, bisel, contorno, transparencias parciales)
- Colocar sobre fondos de bajo contraste
- Recrear la tipografía del logo en otro tipo de letra

---

## 3. Sistema de color

### Primario — Marino (Navy)

| Token | Hex | Uso |
|---|---|---|
| `navy-50` | `#D8E8F2` | Fondos de sección muy claros (modo claro) |
| `navy-100` | `#A8BDD6` | Bordes suaves en modo claro |
| `navy-200` | `#6A8FB8` | Texto secundario en fondos claros |
| `navy-300` | `#3D6099` | Elementos interactivos en fondos claros |
| `navy-700` | `#111E33` | Tarjetas y superficies elevadas sobre navy-900 |
| `navy-800` | `#0D1625` | Tarjetas base, capas intermedias |
| **`navy-900`** | **`#070D1A`** | **Color base de marca — fondo principal** |
| `navy-950` | `#040A12` | Fondos más oscuros, navbars, modales |

### Acento — Dorado (Gold)

| Token | Hex | Uso |
|---|---|---|
| `gold-50` | `#FEF6E8` | Fondos de highlight muy sutiles |
| `gold-100` | `#FCE8C0` | Fondos de badge en modo claro |
| `gold-200` | `#F8D090` | Bordes de énfasis suave |
| `gold-300` | `#F5C060` | Hover state de texto dorado |
| `gold-400` | `#F0B840` | Texto dorado sobre fondos oscuros |
| **`gold-500`** | **`#E8A020`** | **Acento primario — CTAs, íconos activos** |
| `gold-600` | `#C07D10` | Borde de botón dorado |
| `gold-700` | `#975E0B` | Sombra dorada oscura |
| `gold-800` | `#6E4309` | Detalles muy oscuros (raramente usado) |

> **Regla de uso del dorado:** siempre sobre fondos marino o neutros muy oscuros. Nunca sobre blanco puro como color de CTA primario (contraste insuficiente para accesibilidad).

### Neutros — tinte cálido arena

> Refinamiento respecto a la paleta original: se reemplaza el tinte azul-frío por un tinte cálido-arena que complementa el dorado y evita que la interfaz se sienta clínica.

| Token | Hex | Uso |
|---|---|---|
| `neutral-50` | `#F7F6F4` | Fondo blanco cálido (modo claro) |
| `neutral-100` | `#EDECEA` | Fondos de sección en modo claro |
| `neutral-200` | `#D9D8D4` | Bordes en modo claro |
| `neutral-300` | `#C2C0BB` | Texto secundario cálido |
| `neutral-400` | `#A8A5A0` | Placeholder, texto deshabilitado |
| `neutral-500` | `#8C8983` | Texto de apoyo |
| `neutral-600` | `#706D68` | Labels de sección, microcopia |
| `neutral-700` | `#504D49` | Texto oscuro secundario |
| `neutral-800` | `#3D3A37` | Texto oscuro principal en modo claro |
| `neutral-900` | `#272523` | Casi negro — titulares en modo claro |

### Colores semánticos

| Nombre | Hex base | Hex claro (sobre oscuro) | Uso |
|---|---|---|---|
| Éxito | `#3DAA73` | `#5DB88A` | Confirmaciones, estados OK |
| Error | `#E05252` | `#E87272` | Errores, validaciones fallidas |
| Advertencia | `#E8A020` | `#F0B840` | Avisos, expiración, pendientes |
| Información | `#4FA7E8` | `#6DBBEF` | Tips, novedades, datos neutros |

> En interfaz oscura usar siempre el tono **claro** para texto; el tono base solo para la franja/strip de color en tarjetas.

### Variables CSS (custom properties) — lista completa

```css
:root {
  /* Navy */
  --navy-50:  #D8E8F2;
  --navy-100: #A8BDD6;
  --navy-200: #6A8FB8;
  --navy-300: #3D6099;
  --navy-400: #203552;
  --navy-700: #111E33;
  --navy-800: #0D1625;
  --navy-900: #070D1A;
  --navy-950: #040A12;

  /* Gold */
  --gold-50:  #FEF6E8;
  --gold-100: #FCE8C0;
  --gold-200: #F8D090;
  --gold-300: #F5C060;
  --gold-400: #F0B840;
  --gold-500: #E8A020;
  --gold-600: #C07D10;
  --gold-700: #975E0B;
  --gold-800: #6E4309;

  /* Neutrals */
  --neutral-50:  #F7F6F4;
  --neutral-100: #EDECEA;
  --neutral-200: #D9D8D4;
  --neutral-300: #C2C0BB;
  --neutral-400: #A8A5A0;
  --neutral-500: #8C8983;
  --neutral-600: #706D68;
  --neutral-700: #504D49;
  --neutral-800: #3D3A37;
  --neutral-900: #272523;

  /* Semantic */
  --success:   #3DAA73;
  --success-l: #5DB88A;
  --error:     #E05252;
  --error-l:   #E87272;
  --warning:   #E8A020;
  --info:      #4FA7E8;
  --info-l:    #6DBBEF;

  /* Typography */
  --font-display: 'Syne', Arial, sans-serif;
  --font-body:    'DM Sans', Arial, sans-serif;

  /* Spacing (base 4px) */
  --space-1:  4px;
  --space-2:  8px;
  --space-3:  12px;
  --space-4:  16px;
  --space-6:  24px;
  --space-8:  32px;
  --space-10: 40px;
  --space-12: 48px;
  --space-16: 64px;
  --space-20: 80px;
  --space-24: 96px;

  /* Border radius */
  --radius-sm:   4px;
  --radius-md:   8px;
  --radius-lg:   12px;
  --radius-xl:   16px;
  --radius-full: 9999px;

  /* Shadows */
  --shadow-sm:   0 1px 3px rgba(0,0,0,.3);
  --shadow-md:   0 4px 12px rgba(0,0,0,.4);
  --shadow-lg:   0 8px 24px rgba(0,0,0,.5);
  --shadow-gold: 0 0 24px rgba(232,160,32,.3);
  --glow-gold:   0 0 40px rgba(232,160,32,.15);
}
```

---

## 4. Tipografía

### Familias

| Rol | Familia | Fuente |
|---|---|---|
| **Display / Headings** | Syne | Google Fonts |
| **Body / UI** | DM Sans | Google Fonts |

```html
<!-- Importar en HTML -->
<link href="https://fonts.googleapis.com/css2?family=DM+Sans:ital,opsz,wght@0,9..40,300;0,9..40,400;0,9..40,500;0,9..40,600;1,9..40,400&family=Syne:wght@400;600;700;800&display=swap" rel="stylesheet">
```

### Syne — pesos disponibles

| Peso | Valor | Uso |
|---|---|---|
| Regular | 400 | Títulos de bajo énfasis |
| SemiBold | 600 | H3, H4, labels de sección |
| **Bold** | **700** | **H1, H2 — uso principal** |
| ExtraBold | 800 | Display, hero, nombre de marca |

### DM Sans — pesos disponibles

| Peso | Valor | Uso |
|---|---|---|
| Light | 300 | Subtítulos de hero |
| Regular | 400 | Cuerpo de texto general |
| Medium | 500 | Texto de UI, links de nav |
| SemiBold | 600 | Labels, botones secundarios |

### Escala tipográfica

| Step | Tamaño | Peso | Familia | Letter-spacing | Uso |
|---|---|---|---|---|---|
| Display | 72–96px (`clamp`) | 800 | Syne | -0.035em | Hero principal |
| H1 | 48px (`clamp 28–48`) | 700 | Syne | -0.025em | Títulos de página |
| H2 | 36px (`clamp 24–36`) | 700 | Syne | -0.015em | Títulos de sección |
| H3 | 24px | 700 | Syne | 0 | Subtítulos |
| H4 | 18px | 600 | Syne | 0 | Titulares de tarjeta |
| Body L | 18px | 400 | DM Sans | 0 | Lead paragraph |
| Body | 16px | 400 | DM Sans | 0 | Texto general |
| Small | 14px | 400 | DM Sans | 0 | Texto de apoyo |
| Label | 11px | 600 | DM Sans | 0.10em | Labels uppercase |

### Reglas tipográficas

- **Line height titulares**: 1.1–1.2
- **Line height cuerpo**: 1.6–1.7
- **Párrafos largos**: máximo 65–70 caracteres por línea
- **Nunca** usar Syne para cuerpo de texto largo (legibilidad reducida)
- **Nunca** usar DM Sans en pesos mayores a 600 para titulares

---

## 5. Espaciado

Sistema base de **4 px**. Todos los valores son múltiplos exactos.

| Token | Valor | Alias | Uso típico |
|---|---|---|---|
| `space-1` | 4px | micro | Separadores, bordes internos |
| `space-2` | 8px | xs | Ícono + texto inline |
| `space-3` | 12px | sm | Padding de badge/chip |
| `space-4` | 16px | md | Padding de botón, gap compacto |
| `space-6` | 24px | lg | Gap estándar entre elementos |
| `space-8` | 32px | xl | Padding interno de tarjeta |
| `space-10` | 40px | 2xl | Separación entre grupos de contenido |
| `space-12` | 48px | 3xl | Márgenes verticales internos |
| `space-16` | 64px | 4xl | Secciones grandes |
| `space-20` | 80px | 5xl | Hero, separaciones de sección mayor |
| `space-24` | 96px | 6xl | Padding vertical de sección principal |

### Border radius

| Token | Valor | Uso |
|---|---|---|
| `radius-sm` | 4px | Tags pequeños, chips de código |
| `radius-md` | 8px | Botones, inputs, badges |
| `radius-lg` | 12px | Tarjetas compactas, alerts |
| `radius-xl` | 16px | Tarjetas principales, modales |
| `radius-full` | 9999px | Pills, avatares, indicadores |

---

## 6. Efectos y elevación

### Sombras

```css
--shadow-sm:   0 1px 3px rgba(0,0,0,.30);   /* Tarjetas en reposo */
--shadow-md:   0 4px 12px rgba(0,0,0,.40);  /* Hover de tarjeta */
--shadow-lg:   0 8px 24px rgba(0,0,0,.50);  /* Modales, dropdowns */
--shadow-gold: 0 0 24px rgba(232,160,32,.30); /* CTAs primarios en hover */
--glow-gold:   0 0 40px rgba(232,160,32,.15); /* Tarjetas en hover */
```

### Glassmorphism (nav, modales flotantes)

```css
background: rgba(7, 13, 26, 0.88);
backdrop-filter: blur(16px);
border: 1px solid rgba(255,255,255,.08);
```

### Gradiente dorado de énfasis

```css
/* Línea separadora o borde decorativo */
background: linear-gradient(90deg, transparent, rgba(232,160,32,.3), transparent);

/* Resplandor de fondo en hero */
background: radial-gradient(ellipse at 50% -10%, rgba(232,160,32,.09) 0%, transparent 65%);
```

---

## 7. Componentes — patrones de referencia

### Botón primario

```css
background: var(--gold-500);    /* #E8A020 */
color: var(--navy-900);          /* texto marino para contraste */
border-radius: var(--radius-md);
padding: 11px 22px;
font-weight: 600; font-size: 14px;

/* Hover */
background: var(--gold-400);
box-shadow: var(--shadow-gold);
transform: translateY(-1px);
```

### Botón secundario

```css
background: transparent;
color: var(--neutral-100);
border: 1px solid rgba(255,255,255,.18);

/* Hover */
border-color: var(--gold-500);
color: var(--gold-400);
```

### Tarjeta base

```css
background: var(--navy-800);
border: 1px solid rgba(255,255,255,.06);
border-radius: var(--radius-xl);
padding: 24px;

/* Hover */
border-color: rgba(232,160,32,.20);
box-shadow: var(--glow-gold);
```

### Input de formulario

```css
background: var(--navy-900);
border: 1px solid rgba(255,255,255,.10);
border-radius: var(--radius-md);
color: var(--neutral-100);
padding: 11px 14px;

/* Focus */
border-color: var(--gold-500);
box-shadow: 0 0 0 3px rgba(232,160,32,.10);
```

### Badge

```css
/* Gold */
background: rgba(232,160,32,.12);
color: var(--gold-400);
border: 1px solid rgba(232,160,32,.25);
border-radius: var(--radius-full);
padding: 3px 11px;
font-size: 12px; font-weight: 600;
```

---

## 8. Voz y tono

### Personalidad de marca

| Rasgo | Sí | No |
|---|---|---|
| Cercano | "¿Tienes dudas? Hablemos." | "Contáctenos para asesoría." |
| Directo | Oraciones cortas, beneficio primero | Párrafos de relleno |
| Confiable | Datos reales, casos de éxito | Superlativos sin respaldo |
| Ambicioso | Hablar del futuro con fundamento | Promesas imposibles |
| Técnico accesible | Explicar la tecnología en contexto | Jerga sin traducir |

### Ejemplos de escritura

**Sí decimos:**
- *"Digitalizamos tu negocio con lo que necesita, sin obligarte a pagar por lo que no usa."*
- *"Somos el equipo tecnológico que no tenías."*
- *"Con Nexírium tu negocio tiene quién lo respalde, no solo quién le entregue."*

**No decimos:**
- ~~"Potenciamos el ecosistema digital de las PyMEs con soluciones sinérgicas e innovadoras."~~
- ~~"¡Somos los MEJORES desarrolladores de Juárez!"~~
- ~~"Nuestra metodología ágil garantiza deliverables de alta calidad."~~

### Guía por canal

| Canal | Tono | Notas |
|---|---|---|
| Redes sociales | Conversacional, energético | Emojis con criterio. Documenta antes/después. |
| Sitio web | Claro, estructurado | Titulares de beneficio. Sin jerga en zonas públicas. |
| Propuestas | Profesional y cercano | Nombre del cliente siempre presente. Cierra con próximos pasos. |
| Soporte / app | Útil, tranquilizador | Errores nunca son culpa del usuario. Siempre da una salida. |

---

## 9. Archivos de marca

| Archivo | Formato | Contenido |
|---|---|---|
| `IMAGOTIPO.svg` | SVG | Símbolo + nombre · versión principal |
| `LOGOTIPO.svg` | SVG | Solo nombre |
| `ISOTIPO.svg` | SVG | Solo símbolo |
| `POSITIVO_NEGATIVO.pdf` | PDF | Guía de variaciones positivo/negativo |
| `BRAND_GUIDE.html` | HTML | Guía visual interactiva |
| `BRAND_GUIDELINES.md` | MD | Este documento |

---

## 10. Control de versiones

| Versión | Fecha | Cambios |
|---|---|---|
| 1.0 | Mayo 2026 | Identidad inicial. Paleta refinada con escalas completas y neutros cálidos. Guía de voz y tono. Biblioteca de componentes base. |

---

*Nexírium · Ciudad Juárez, Chih., México · Documento confidencial de uso interno*
