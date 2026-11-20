# Guía Visual de AgentHub

**Documento:** Sistema Visual Unificado  
**Versión:** 1.0  
**Fecha:** Noviembre 2024  
**Propósito:** Referencia visual principal para implementación y mantenimiento

---

## 1. Visión General

Este documento define las decisiones visuales y de diseño para AgentHub, una plataforma SaaS empresarial para gestionar agentes de inteligencia artificial. 

**Prioridades:**
1. Excelente acabado visual y experiencia premium
2. Fidelidad a las referencias de Google Stitch
3. Coherencia visual en las seis secciones
4. Calidad equivalente en tema claro y oscuro
5. Implementación sencilla y mantenible

---

## 2. Identidad Visual Global

### Tipografía

**Fuentes:**
- **Interfaz (UI):** Geist (sans-serif moderna, legible, con tracking negativo en titulares)
- **Datos/Código/Telemetría:** JetBrains Mono (monoespaciada para valores numéricos, timestamps, IDs)

**Jerarquía de Tamaños (Geist):**

| Nivel | Tamaño | Peso | Tracking | Uso |
|-------|--------|------|----------|-----|
| **Display** | 36px / 2.25rem | 600 | -0.03em | Títulos principales (rarely used) |
| **Headline XL** | 28px / 1.75rem | 700 | -0.025em | Títulos de página principales |
| **Headline LG** | 24px / 1.5rem | 600 | -0.02em | Títulos de secciones |
| **Headline MD** | 20px / 1.25rem | 600 | -0.015em | Encabezados de tarjetas |
| **Headline SM** | 16px / 1rem | 600 | -0.01em | Subtítulos, labels en componentes |
| **Body LG** | 16px / 1rem | 400 | 0 | Cuerpo principal, tablas |
| **Body MD** | 14px / 0.875rem | 400 | -0.005em | Descripciones, cuerpo secundario |
| **Body SM** | 12px / 0.75rem | 400 | 0 | Textos pequeños, auxiliares |
| **Label MD** | 14px / 0.875rem | 500 | 0.02em | Etiquetas de campos, metadata |
| **Label SM** | 12px / 0.75rem | 500 | 0.03em | Badges, chips, timestamp |

**JetBrains Mono (Monoespaciada):**
- **Code SM:** 12px, 400, line-height 1.5
- **Code XS:** 11px, 500, line-height 1.25
- Uso: valores numéricos en tablas (con `font-variant-numeric: tabular-nums`), stack traces, IDs técnicos

**Reglas Tipográficas:**
- Usar `font-variant-numeric: tabular-nums` en todos los valores numéricos para evitar jitter
- Tracking negativo en titulares reduce espaciado visual y aumenta densidad
- Monoespaciada obligatoria para código, latencias, IDs de agente

---

### Paleta de Colores — Light Mode

**Superficies y Fondos:**

| Elemento | Valor | Tailwind |
|----------|-------|----------|
| Canvas de fondo | `#faf8ff` | slate-50 con tint indigo |
| Superficie principal | `#ffffff` | white |
| Superficie secundaria 1 | `#f2f3ff` | indigo-50 |
| Superficie secundaria 2 | `#eaedff` | indigo-100 |
| Borde estructural | `#e2e8f0` | slate-200 |
| Borde hover | `#cbd5e1` | slate-300 |

**Texto:**

| Elemento | Valor | Tailwind |
|----------|-------|----------|
| Texto principal | `#131b2e` | slate-900 |
| Texto secundario | `#334155` | slate-700 |
| Texto terciario/metadata | `#64748b` | slate-500 |
| Placeholder | `#94a3b8` | slate-400 |

**Accentes Funcionales:**

| Estado | Valor | Tailwind | Uso |
|--------|-------|----------|-----|
| **Primario** | `#4f46e5` | indigo-600 | Acciones, toggles, enlaces, focos |
| **Primario Hover** | `#4338ca` | indigo-700 | Estados hover de botones |
| **Primario Light** | `#6366f1` | indigo-500 | Hover suave, backgrounds |
| **Éxito** | `#059669` | emerald-600 | Estados activos, healthy |
| **Éxito BG** | `#ecfdf5` | emerald-50 | Background de badges verdes |
| **Advertencia** | `#d97706` | amber-600 | Warnings, degraded |
| **Advertencia BG** | `#fffbeb` | amber-50 | Background de badges amarillas |
| **Error** | `#e11d48` | rose-600 | Errores, críticos |
| **Error BG** | `#fff1f2` | rose-50 | Background de badges rojas |

---

### Paleta de Colores — Dark Mode

**Superficies y Fondos:**

| Elemento | Valor | Tailwind |
|----------|-------|----------|
| Canvas de fondo | `#0b1326` | slate-950 con tint violet |
| Superficie principal | `#131b2e` | slate-900 |
| Superficie elevada | `#1e293b` | slate-800 |
| Superficie overlay | `#222a3d` | slate-800 |
| Borde estructural | `#2d3449` | slate-700 |
| Borde hover | `#3f46e1` | indigo-500 con opacity |

**Texto:**

| Elemento | Valor | Tailwind |
|----------|-------|----------|
| Texto principal | `#dae2fd` | indigo-50 |
| Texto secundario | `#908fa0` | slate-400 |
| Texto terciario/metadata | `#64748b` | slate-500 |
| Placeholder | `#475569` | slate-600 |

**Accentes Funcionales:**

| Estado | Valor | Tailwind | Uso |
|--------|-------|----------|-----|
| **Primario** | `#c0c1ff` | indigo-300 | Acciones, toggles, enlaces |
| **Primario Hover** | `#a5a6f6` | indigo-400 | Estados hover |
| **Éxito** | `#10b981` | emerald-500 | Estados activos |
| **Éxito BG** | `#064e3b` | emerald-900 | Background de badges verdes |
| **Advertencia** | `#f59e0b` | amber-500 | Warnings |
| **Advertencia BG** | `#78350f` | amber-900 | Background de badges amarillas |
| **Error** | `#f43f5e` | rose-500 | Errores |
| **Error BG** | `#7f1d1d` | rose-900 | Background de badges rojas |

**Regla: Aplicar clase `dark` a elemento raíz (`html` o `body`) para activar Dark Mode.**

---

### Dimensiones y Espaciado

**Border Radius (Redondeadores):**

| Componente | Valor | Tailwind | Uso |
|-----------|-------|----------|-----|
| Botones, inputs, chips | `0.5rem` | rounded-lg | Componentes interactivos |
| Tarjetas, contenedores | `1rem` | rounded-xl | Paneles principales |
| Modales, overlays | `1.5rem` | rounded-2xl | Capas flotantes |
| Status pills/badges | `9999px` | rounded-full | Indicadores de estado |

**Espaciado (8px base rhythm):**

| Escala | Valor | Tailwind | Contexto |
|--------|-------|----------|----------|
| XS | 0.25rem | space-1 | Gaps mínimos |
| SM | 0.5rem | space-2 | Separaciones menores |
| MD | 1rem | space-4 | Espaciado base |
| LG | 1.5rem | space-6 | Espaciado generoso |
| XL | 2rem | space-8 | Separaciones grandes |

**Márgenes de Canvas:**

| Breakpoint | Desktop | Tablet | Mobile |
|-----------|---------|--------|--------|
| Margen externo | 2rem (32px) | 1.5rem (24px) | 1rem (16px) |
| Gutter (columnas) | 1.5rem (24px) | 1.25rem (20px) | 1rem (16px) |
| Padding card | 1rem - 1.5rem | 1rem | 0.75rem |

---

## 3. Componentes Base

### Botones

**Especificaciones Generales:**
- Height: 40px mínimo (touch-friendly)
- Padding: `px-3.5 py-2` / `0.875rem 0.5rem`
- Font: Geist, weight 500, size `label-sm`
- Border radius: `rounded-lg` (8px)
- Transiciones suaves: `transition-all 200ms`

**Estados Visuales:**

#### Primary (Acción Principal)
- **Default:** BG indigo-600 / Text white
- **Hover:** BG indigo-700, escala ligera
- **Focus:** Ring 2px indigo-500/20
- **Active:** Scale 0.99 (press feedback)
- **Disabled:** Opacity 50%, cursor no-change

#### Secondary (Acción Secundaria)
- **Default:** BG white, Border 1px slate-200, Text slate-900
- **Hover:** BG slate-50, Border slate-300
- **Focus:** Ring 2px indigo-500/20
- **Dark mode:** BG slate-900, Border slate-700, Text slate-100

#### Destructive (Eliminar/Riesgo)
- **Default:** BG rose-50, Text rose-600, Border 1px rose-300
- **Hover:** BG rose-100, Text rose-700
- **Focus:** Ring 2px rose-500/20
- **Dark mode:** BG rose-500/10, Text rose-400, Border rose-500/30

#### Ghost (Acción Mínima)
- **Default:** BG transparent, Text slate-600
- **Hover:** BG slate-100, Text slate-900
- **Dark mode hover:** BG slate-800, Text slate-100

---

### Campos de Formulario

**Text Input / Textarea:**
- Height: 40px (input), auto (textarea)
- Padding: `0.75rem` horizontal, `0.5rem` vertical
- BG: white (light) / slate-900/60 (dark)
- Border: 1px solid, slate-200 (light) / slate-800 (dark)
- Border radius: `rounded-lg`
- Text: slate-900 (light) / slate-100 (dark)
- Placeholder: slate-400 (light) / slate-500 (dark)
- **Focus:** Border indigo-600, ring 3px rgba(79, 70, 229, 0.12)
- Font: Geist, `body-md`

**Select / Dropdown Trigger:**
- Mismo estilo que text input
- Icono dropdown a la derecha (margin-right: 8px)
- Opciones: white BG (light) / slate-800 (dark)

---

### Badges y Estados

**Status Badges (Pills):**
- Height: 24px (`1.5rem`)
- Padding: `0 0.625rem`
- Font: JetBrains Mono, `label-sm` (12px, 500), uppercase
- Border radius: `rounded-full`
- Border: 1px solid
- Formato: `[Status] [Value]` con icono opcional

**Estados Predefinidos:**

| Estado | Light BG | Light Text | Dark BG | Dark Text | Icono |
|--------|----------|-----------|---------|-----------|-------|
| **Active/Success** | `#ecfdf5` | `#047857` | `#064e3b` | `#10b981` | ✓ pulsing |
| **Warning** | `#fffbeb` | `#b45309` | `#78350f` | `#f59e0b` | ⚠ |
| **Error/Critical** | `#fff1f2` | `#be123c` | `#7f1d1d` | `#f43f5e` | ✕ |
| **Neutral/Idle** | `#f1f5f9` | `#475569` | `#334155` | `#cbd5e1` | - |

---

### Tarjetas (Cards)

**Especificaciones:**
- Border radius: `rounded-xl` (16px)
- Border: 1px solid, slate-200 (light) / slate-800 (dark)
- BG: white (light) / slate-900 (dark)
- Padding: `1rem` (space-md) o `1.5rem` (space-lg) según jerarquía
- Shadow: `0 1px 3px rgba(0,0,0,0.1)` (light), `0 1px 3px rgba(0,0,0,0.3)` (dark)
- **Hover:** Border a slate-300 (light) / slate-700 (dark), shadow aumenta, translate-y -1px

**Variantes:**
- **Primary Card:** Padding `space-lg`, shadow mayor
- **Standard Card:** Padding `space-md`
- **Muted Card:** BG slate-50 (light) / slate-800/40 (dark)

---

### Tablas

**Estructura:**
- Border outer: `1px solid` slate-200 (light) / slate-800 (dark)
- Border radius: `rounded-lg`
- Overflow: hidden
- Background: white (light) / slate-900 (dark)

**Header Row:**
- BG: slate-50 (light) / slate-800 (dark)
- Text: JetBrains Mono, `label-sm`, uppercase
- Tracking: wider
- Padding: `0.75rem 1rem`
- Border-bottom: `1px solid` slate-200 (light) / slate-700 (dark)
- Font weight: 500

**Data Rows:**
- Height: 48px mínimo
- Padding: `0.75rem 1rem`
- Border-bottom: `1px solid` slate-100 (light) / slate-800 (dark)
- Text: Geist, `body-md`
- **Hover:** BG slate-50 (light) / slate-800/40 (dark)
- **Last row:** Sin border-bottom

**Columnas Numéricas:**
- Alineación: `text-right`
- Font: JetBrains Mono (con `tabular-nums`)
- Color: slate-700 (light) / slate-300 (dark)

---

### Modales

**Estructura:**
- Border radius: `rounded-2xl` (24px)
- BG: white (light) / slate-900 (dark)
- Border: 1px solid slate-200 (light) / slate-700 (dark)
- Padding: `2rem` interior
- Backdrop: `rgba(0,0,0,0.4)` con `backdrop-filter: blur(4px)`
- Shadow: `0 20px 25px -5px rgba(0,0,0,0.1)`, `0 8px 10px -6px rgba(0,0,0,0.04)`

**Componentes Internos:**
- **Header:** Flex between, título `headline-md`, botón X (`rounded-lg`)
- **Body:** Contenido principal, padding vertical
- **Footer:** Botones de acción, flex gap-md

**Comportamiento:**
- Cierre: botón X, Escape key, clic en backdrop
- Animación: fade-in (opacity 0→1), fade-out
- Z-index: modal 1000, backdrop 999

---

## 4. Diseño de las Seis Secciones

### 4.1 Dashboard

**Composición Visual:**

1. **Tarjetas de KPI (4 columnas - Desktop, 2 - Tablet, 1 - Mobile)**
   - Cada tarjeta: `rounded-xl`, `p-space-lg`
   - Encabezado con label (uppercase, `label-sm`) y badge de estado
   - Valor principal (28px, bold indigo en light, indigo-300 en dark)
   - Subtítulo explicativo (12px, slate-500)
   - Icono a la derecha (opcional, hover scale)
   - Gradient sutil de fondo (decorativo, blur)

2. **Sección de Actividad (2 partes):**
   - **Gráfico (8 columnas desktop):** Tarjeta con título, descripción, leyenda, SVG/Canvas para gráfico
   - **Tabla (4 columnas desktop):** Card con tabla de últimos eventos

3. **Consistencia:**
   - Espaciado uniforme entre tarjetas: `gap-space-lg`
   - Colores de fondos sutiles para cada KPI (error/tertiary backgrounds con opacity)
   - Estados hover uniformes

---

### 4.2 Gestión de Usuarios

**Composición:**
- Encabezado con título y botón de crear usuario (opcional)
- **Tabla principal:**
  - Columnas: Nombre, Email, Plan, Estado
  - Fila seleccionable (highlight en hover)
  - Menú de acciones (3 dots) con opciones: "Ver Detalle", "Eliminar"
  
- **Modal de Detalle:**
  - Nombre, Email, Plan, Estado
  - Fecha de registro
  - Información ficticia de cuenta (última login, etc.)
  - Botones: Desactivar, Eliminar

- **Modal de Confirmación (Eliminar):**
  - Texto rojo, pregunta clara
  - Botones: Cancelar, Confirmar Eliminación (rojo)

---

### 4.3 Gestión de Agentes

**Composición:**
- Encabezado con título y filtros (opcional)
- **Listado de Agentes (cards o filas):**
  - Nombre del agente, Propietario
  - Estado (badge): Activo (verde), Inactivo (gris), Fallando (rojo)
  - Sección de Skills (colapsable):
    - Por defecto colapsado
    - Al expandir muestra lista de skills con versión
    - Contenedor con borde izquierdo indigo para profundidad
  - Botones de acción: "Configurar" (Primary), "Eliminar" (Destructive)

- **Modal de Configuración:**
  - Título: "Configurar Agente"
  - Campo: System Prompt (textarea multilinea, monoespaciada)
  - Botones: Guardar (Primary), Cancelar
  - Feedback visual tras guardar

---

### 4.4 Catálogo de Skills

**Composición:**
- Sección introductoria: "¿Qué es una skill?" (explicación breve)
- **Tabla de Skills:**
  - Columnas: Nombre, Descripción, Agentes Usando
  - Descripciones cortas y legibles
  - Número de agentes en badge o numero simple
  - Botones: "Ver Detalle", "Eliminar"

- **Modal de Detalle:**
  - Nombre de skill
  - Descripción completa
  - Parámetros técnicos ficticios
  - Lista de agentes que usan
  - Fecha de creación

---

### 4.5 Contrataciones

**Composición:**
- **Tabla de Contratos:**
  - Columnas: Cliente, Agente, Skills, Fecha Inicio, Fecha Fin, Importe Total
  - Datos coherentes (fechas, montos en USD)
  - Botón: "Ver Detalle"

- **Modal de Detalle:**
  - Información del cliente
  - Agente contratado
  - Fechas (con duración)
  - **Desglose de Precios:**
    - Precio base del agente
    - Precio individual por skill (tabla anidada)
    - Subtotal
    - Descuentos (si aplica)
    - Impuestos
    - **Total (highlight)**
  - Historial de pagos ficticios

---

### 4.6 Log de Errores

**Composición:**
- **Tabla de Errores:**
  - Columnas: Timestamp, Agente, Tipo, Descripción, Estado
  - Tipos color-coded: Crítico (rojo), Advertencia (amarillo), Información (azul)
  - Estados: Pendiente (normal), Resuelto (verde + checkmark)
  - Botones: "Ver Detalle", "Marcar como Resuelto"

- **Modal de Detalle:**
  - Timestamp completo
  - Agente involucrado
  - Tipo con badge
  - Descripción
  - **Stack Trace (contenedor monoespaciado):**
    - Fondo gris/oscuro
    - Texto JetBrains Mono
    - Formato: archivo.ts:123, función(), mensaje
  - Botón: "Marcar como Resuelto"
  - Errores resueltos muestran checkmark verde

---

## 5. Comportamientos Visuales

### Transiciones
- Duración base: 200ms
- Función: `ease-in-out`
- Propiedades: `all` (borders, bg, shadow)
- Evitar: animaciones complejas, parallax innecesario

### Hover States
- Tarjetas: elevación (+shadow), border color más claro
- Botones: escala 0.99, shadow
- Filas de tabla: BG color
- Links/elementos interactivos: underline o color change

### Focus States
- Ring: 2px indigo-500 con opacity 20%
- Visible en: inputs, botones, links
- Offset: 2px
- Keyboard navigation: navigation visible sempre

### Loading States (si aplica)
- Spinner indigo animado
- Skeleton: BG gradient pulse
- Texto: opacity 50% si está deshabilitado

---

## 6. Responsive Design

### Breakpoints
- **Desktop:** 1280px+ (1 sidebar fijo, 2-4 columnas contenido)
- **Tablet:** 768px - 1279px (sidebar colapsable, 2 columnas)
- **Mobile:** < 768px (drawer off-canvas, 1 columna, full-width)

### Comportamientos por Tamaño

**Sidebar:**
- Desktop: visible, ancho fijo 256px
- Tablet: colapsable a 64px (icon-only)
- Mobile: drawer off-canvas (full-height, overlay)

**Tablas:**
- Desktop: horizontal scroll si necesario
- Tablet: filas comprimidas
- Mobile: convertir a cards apiladas vertical

**Modales:**
- Desktop: ancho máx 600px, centrado
- Tablet: ancho 90vw
- Mobile: full-screen o casi full-screen con padding

**Tarjetas (Dashboard):**
- Desktop: 4 columnas
- Tablet: 2 columnas
- Mobile: 1 columna (stack)

---

## 7. Accesibilidad

### Contraste
- **WCAG AAA:** Texto principal sobre fondos (ratio 7:1)
- **WCAG AA:** Elementos interactivos (ratio 4.5:1)
- **Prueba:** Verificar con herramientas de contraste Chrome DevTools

### Navegación por Teclado
- **Tab order:** Lógico, siguiendo flujo visual
- **Focus outline:** Visible en todos los elementos interactivos
- **Escape:** Cierra modales y dropdowns
- **Enter:** Activa botones
- **Arrow keys:** Navegación en dropdowns, selects

### Labels y Descripciones
- Todos los inputs tienen labels explícitos (no solo placeholder)
- Aria-label en iconos sin texto
- Descripciones de error claras en validaciones
- Timestamps en formato legible (ej. "Nov 20, 2024 14:30")

---

## 8. Persistencia Visual

### localStorage - Preferencias
- **Tema:** Guardar selección Light/Dark (key: `agenthub-theme`)
- **Preferencias:** Sidebar colapsado/expandido (key: `agenthub-sidebar-collapsed`)

### localStorage - Datos Simulados
- **System Prompts:** Cambios en edición de agentes (key: `agenthub-agent-{id}-system-prompt`)
- **Errores Resueltos:** Estado de resolución (key: `agenthub-error-{id}-resolved`)
- **Registros Eliminados:** Marcar como eliminados (key: `agenthub-{section}-{id}-deleted`)

**Regla:** Cambios visuales relacionados con datos persisten en localStorage sin confirmación adicional.

---

## 9. Implementación

### Stack Requerido
- HTML5 (semántico)
- Tailwind CSS v4 via CDN
- JavaScript ES6+ vanilla (sin transpilación)
- **Sin frameworks** (React, Vue, Angular)
- **Sin librerías adicionales**

### Reglas de Código
- Reutilizar estilos y componentes existentes
- Usar clases Tailwind sin extensiones complejas
- Mantener código legible y sencillo
- Evitar animaciones y efectos innecesarios
- Priorizar funcionalidad sobre perfeccionismo visual

### Estructura de Componentes
Usar patrones recurrentes:

```html
<!-- Card Base -->
<div class="rounded-xl border border-slate-200 dark:border-slate-800 bg-white dark:bg-slate-900 p-space-lg shadow-sm hover:shadow-md transition-all">
  <!-- Content -->
</div>

<!-- Button Primary -->
<button class="bg-indigo-600 hover:bg-indigo-700 text-white rounded-lg px-3.5 py-2 transition-all focus:ring-2 focus:ring-indigo-500/20">
  Acción
</button>

<!-- Status Badge -->
<span class="inline-flex items-center gap-1 px-2.5 py-0.5 rounded-full text-label-xs font-semibold bg-emerald-50 text-emerald-700 dark:bg-emerald-900/30 dark:text-emerald-400">
  ✓ Activo
</span>
```

---

## 10. Instrucción para Futuras Implementaciones

**IMPORTANTE: Consultar `specs-AgentHub/DESIGN.md` ANTES de implementar o modificar el diseño de cualquier sección.**

Este documento es la única referencia visual oficial de AgentHub. Garantiza coherencia, calidad y eficiencia en la implementación.

### Checklist Previo a Implementación

Antes de escribir CSS o HTML para cualquier sección:

- [ ] Revisar la sección correspondiente en DESIGN.md (ej. 4.2 para Gestión de Usuarios)
- [ ] Consultar componentes base (sección 3)
- [ ] Verificar paleta de colores (Light y Dark)
- [ ] Revisar espaciado, tipografía y comportamientos
- [ ] Estudiar referencias HTML en `stich-reference/` si aplica
- [ ] Usar únicamente Tailwind CSS sin personalizaciones
- [ ] No improvisar estilos distintos
- [ ] No realizar rediseños innecesarios
- [ ] Mantener coherencia visual con el resto de la aplicación

### Validación de Calidad Visual

Después de implementar:

- [ ] Verificar en Desktop (1280px+), Tablet (768px), Mobile (<768px)
- [ ] Comprobar tema Light y Dark Mode
- [ ] Verificar hover states, focus states, estados deshabilitados
- [ ] Revisar alineación, espaciado y typografía
- [ ] Confirmar accesibilidad (contraste, navegación teclado)
- [ ] Verificar que no hay desbordes o elementos cortados
- [ ] Revisar coherencia con otras secciones
- [ ] No hay errores en consola

---

## 11. Referencia Rápida de Colores

### Light Mode (Por Categoría)

**Neutros:**
```
Canvas:     #faf8ff
Surface:    #ffffff
Secondary:  #f2f3ff
Border:     #e2e8f0
Text:       #131b2e
Text alt:   #334155
Muted:      #64748b
```

**Acciones:**
```
Primary:    #4f46e5
Primary-h:  #4338ca
Focus:      ring-indigo-500/20
```

**Funcionales:**
```
Success:    #059669 (bg: #ecfdf5)
Warning:    #d97706 (bg: #fffbeb)
Error:      #e11d48 (bg: #fff1f2)
```

### Dark Mode (Por Categoría)

**Neutros:**
```
Canvas:     #0b1326
Surface:    #131b2e
Elevated:   #1e293b
Border:     #2d3449
Text:       #dae2fd
Text alt:   #908fa0
Muted:      #64748b
```

**Acciones:**
```
Primary:    #c0c1ff
Primary-h:  #a5a6f6
Focus:      ring-indigo-400/50
```

**Funcionales:**
```
Success:    #10b981 (bg: #064e3b)
Warning:    #f59e0b (bg: #78350f)
Error:      #f43f5e (bg: #7f1d1d)
```

---

## 12. Resumen de Decisiones Visuales Principales

| Aspecto | Decisión |
|---------|----------|
| **Tipografía UI** | Geist (sans-serif moderna) |
| **Tipografía Datos** | JetBrains Mono (monoespaciada) |
| **Colores primarios** | Indigo/Violet en ambos temas |
| **Border Radius** | 8px buttons, 16px cards, 24px modales |
| **Espaciado base** | 8px rhythm (1rem = 16px) |
| **Profundidad** | Borders + subtle shadows |
| **Animaciones** | 200ms suaves, ease-in-out |
| **Tema oscuro** | Clase `dark` en raíz |
| **Responsive** | Desktop 1280px+, Tablet 768px, Mobile <768px |
| **Accesibilidad** | WCAG AAA, keyboard nav, focus visible |
| **Persistencia** | localStorage (tema, preferencias, datos) |

---

**Documento finalizado:** Noviembre 2024

**Próxima revisión:** Cuando haya cambios significativos en la identidad visual o nuevos componentes introducidos.

