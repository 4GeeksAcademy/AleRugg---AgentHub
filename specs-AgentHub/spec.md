# Especificación Funcional de AgentHub

**Versión:** 1.0  
**Fecha:** Noviembre 2024  
**Estado:** Especificación técnica y funcional

---

## 1. Visión General del Producto

**AgentHub** es una plataforma SaaS (Software as a Service) empresarial que permite a las organizaciones contratar, configurar y administrar agentes de inteligencia artificial. Los agentes son entidades autónomas dotadas de capacidades especializadas (skills) que pueden ejecutar tareas, automatizaciones y análisis complejos.

La plataforma proporciona un panel administrativo centralizado para supervisar el desempeño de agentes, gestionar usuarios, configurar capacidades, revisar contratos activos y analizar errores operativos en tiempo real.

### Propósito
- Centralizar la gestión de múltiples agentes de IA bajo una interfaz unificada
- Facilitar la contratación y facturación de servicios de agentes
- Monitorear la salud operativa y rendimiento de agentes
- Proporcionar visibilidad sobre costos, ingresos y actividad

---

## 2. Stack Tecnológico

### Requisitos Obligatorios
- **Lenguaje de marcado:** HTML5 (semántico, accesible)
- **Estilos:** Tailwind CSS v4 mediante CDN
- **Interactividad:** JavaScript ES6+ vanilla (sin transpilación)
- **Restricciones:** Sin React, Vue, Angular, ni frameworks de UI
- **Librerías externas:** Ninguna (excepto Tailwind CSS y fuentes tipográficas)
- **Backend:** No aplica
- **Base de datos:** No aplica
- **APIs:** No aplica
- **Build/Compilación:** No aplica
- **Dependencias de Node.js/npm:** No aplica

### Ejecución
- Aplicación SPA (Single Page Application) que se ejecuta completamente en el navegador
- Servidor web simple (Python Flask incluido en el repositorio) para servir archivos estáticos
- Datos ficticios generados en memoria

### Persistencia
- **localStorage** para guardar preferencias y cambios simulados
- Ausencia de sincronización con backend
- Reset manual posible mediante console o devtools

---

## 3. Identidad Visual y Diseño

### Principios de Diseño
- **Estética:** SaaS empresarial premium, inspirado en Google Stitch
- **Paleta:** Indigo/Violet como identidad primaria
- **Estilo:** Moderno, técnico, profesional, con jerarquía visual clara
- **Densidad:** Densa sin abrumar; optimizada para escaneo rápido de datos
- **Accesibilidad:** Contraste WCAG AAA para textos, AA para elementos interactivos

### Tipografía
- **Interfaz (UI):** Geist (sans-serif moderna y legible)
- **Datos/Código/Telemetría:** JetBrains Mono (monoespaciada)
- **Figuras:** Tabular (`font-variant-numeric: tabular-nums`) para números en tablas

### Paleta de Colores

#### Light Mode
| Elemento | Valor |
|----------|-------|
| Canvas de fondo | `#faf8ff` |
| Superficies principales | `#ffffff` |
| Superficies secundarias | `#f2f3ff`, `#eaedff` |
| Bordes estructurales | `#e2e8f0` |
| Texto principal | `#131b2e` |
| Texto secundario | `#334155` |
| Acento primario (acciones) | `#4f46e5` (Indigo 600) |
| Éxito/Activo | `#059669` (Emerald 600) |
| Advertencia | `#d97706` (Amber 600) |
| Error/Crítico | `#e11d48` (Rose 600) |

#### Dark Mode
| Elemento | Valor |
|----------|-------|
| Canvas de fondo | `#0b1326` |
| Superficies principales | `#131b2e` |
| Superficies elevadas | `#1e293b` |
| Bordes estructurales | `#2d3449` |
| Texto principal | `#dae2fd` |
| Texto secundario | `#908fa0` |
| Acento primario | `#c0c1ff` (Indigo 300) |
| Éxito/Activo | `#10b981` (Emerald 500) |
| Advertencia | `#f59e0b` (Amber 500) |
| Error/Crítico | `#f43f5e` (Rose 500) |

**Nota:** El tema oscuro se activa aplicando la clase `dark` al elemento raíz.

### Radiuses (Redondeadores)
- Botones, inputs, chips: `0.5rem` (8px)
- Tarjetas, contenedores: `1rem` (16px)
- Modales, overlays: `1.5rem` (24px)
- Status badges (pills): `9999px` (redondo completo)

### Espaciado
- Gutter (columnas): `1.5rem` (24px) - Desktop, `1rem` (16px) - Mobile
- Margen canvas: `2rem` (32px) - Desktop, `1rem` (16px) - Mobile
- Padding interno: `1rem`, `1.5rem`, `2rem`

---

## 4. Arquitectura de Pantallas

### 4.1 Dashboard

**Propósito:** Proporcionar una visión de alto nivel de la salud operativa y métricas clave de la plataforma.

#### Indicadores Clave (KPIs)
Se presentan en cuatro tarjetas destacadas:

1. **Ingresos Totales del Mes**
   - Valor numérico en moneda (ej. $45,320.00)
   - Período: Mes actual
   - Icono o indicador de tendencia

2. **Pérdidas por Descuentos y Cupones**
   - Valor numérico negativo
   - Desglose opcional por tipo

3. **Agentes Activos**
   - Contador de agentes con estado "activo"
   - Porcentaje vs. total

4. **Agentes Fallando**
   - Contador de agentes con estado "fallando"
   - Indicador visual de criticidad

#### Gráfico de Actividad Semanal
- **Eje X:** Últimos 7 días (Mon-Sun)
- **Eje Y:** Número de ejecuciones/actividad
- **Tipo:** Gráfico de barras o línea
- **Datos:** Ficticios pero consistentes

#### Tabla de Actividad Reciente
Muestra los eventos más recientes de los agentes en un formato profesional y bien jerarquizado:

| Columna | Descripción | Formato/Notas |
|---------|-------------|---------------|
| **Timestamp** | Fecha y hora del evento | Formato: "Nov 20, 2024 14:30" (JetBrains Mono para hora) |
| **Agente** | Nombre del agente que ejecutó la acción | Texto normal, con identidad visual clara |
| **Acción** | Tipo de actividad | Opciones: "Ejecución", "Completado", "Error", "Reinicio", "Cancelado" |
| **Duración** | Tiempo de ejecución | Formato: "2.5s", "15ms", "1m 30s" (en monoespaciada) |
| **Estado** | Resultado de la acción | Badge: Éxito (verde), Fallo (rojo), En progreso (azul) |

**Requisitos de la Tabla:**
- Debe mostrar mínimo 10 filas de datos ficticios coherentes
- Encabezados: uppercase, semibold, fondo sutil (Light: `#f1f5f9`, Dark: `#1e293b`)
- Filas alternadas: color de fondo coherente en hover
- Timestamps en columna izquierda para legibilidad de escaneo rápido
- Badges de estado claramente diferenciados por color
- Valores numéricos (duración) alineados a la derecha
- Bordes claros entre filas para separación visual
- Responsive: en mobile, convertir a cards apiladas si es necesario

**Datos Ficticios:**
Ejemplos de filas:
- "Nov 20, 2024 14:35" | "DataBot" | "Ejecución" | "2.5s" | Éxito ✓
- "Nov 20, 2024 14:28" | "WebScraperAI" | "Completado" | "12.8s" | Éxito ✓
- "Nov 20, 2024 14:15" | "AnalysisBot" | "Error" | "0.3s" | Fallo ✗
- "Nov 20, 2024 14:02" | "CalendarBot" | "En progreso" | "5.2s..." | En progreso

#### Comportamiento
- Carga automática de datos ficticios al abrir Dashboard
- Tabla permanece visible y legible en ambos temas
- Actualización simulada cada intervalo (opcional, no es requisito)
- Scroll horizontal en mobile si es necesario (con advertencia visual)
- Fila seleccionable produce highlight visual (opcional, no requiere acción)

---

### 4.2 Gestión de Usuarios

**Propósito:** Administrar cuentas de usuario, planes contratados y estado de suscripción.

#### Tabla Principal
Presenta todos los usuarios activos y suscritos:

| Columna | Contenido |
|---------|-----------|
| **Nombre** | Nombre completo del usuario |
| **Email** | Dirección de correo |
| **Plan** | Plan activo (Starter, Professional, Enterprise) |
| **Estado** | Activo, Inactivo, Cancelado |

#### Acciones por Fila
- **Ver Detalle:** Abre modal con información completa
- **Eliminar:** Solicita confirmación antes de proceder

#### Modal de Detalle del Usuario
Muestra:
- Nombre completo
- Email
- Plan activo
- Estado (Activo/Inactivo/Cancelado)
- Fecha de registro
- Información ficticia de cuenta (límites, uso actual, etc.)
- Botones de acción: Editar, Desactivar, Eliminar

#### Confirmación de Eliminación
- Modal con pregunta explícita
- Texto de advertencia en rojo
- Botón de confirmación claramente destructivo
- Opción de cancelar

---

### 4.3 Gestión de Agentes

**Propósito:** Configurar, monitorear y administrar agentes de IA dentro de la plataforma.

#### Listado de Agentes
Presentación en formato de tarjetas o tabla compacta:

| Campo | Contenido |
|-------|-----------|
| **Nombre** | Identificador/alias del agente |
| **Propietario** | Usuario o equipo que administra el agente |
| **Estado** | Activo, Inactivo, Fallando |
| **Skills Habilitadas** | Lista colapsable de capacidades |

#### Collapsible Skills
Elemento expandible que muestra información detallada de las skills asociadas al agente:

**Estado Inicial (Colapsado):**
- Encabezado visible con icono de expansión (▼ / ▶)
- Texto: "Skills" o "Capacidades" seguido del icono
- Color de fondo: sutil (Light: `#f1f5f9`, Dark: `#1e293b`)
- Border radius: `0.5rem`
- Altura mínima: 44px (touch-friendly)

**Estado Expandido:**
Muestra lista de skills con información:

| Campo | Descripción | Formato |
|-------|-------------|---------|
| **Nombre** | Nombre de la skill | Texto normal, semibold |
| **Descripción** | Función o utilidad de la skill | Texto pequeño, secundario |
| **Estado** | Si está habilitada o deshabilitada | Badge: Habilitada (verde), Deshabilitada (gris) |

**Ejemplo de Contenido Expandido:**
```
✓ Web Browsing
  Permite a agentes navegar por internet y extraer información
  [Habilitada]

✓ Document Analysis
  Lectura y análisis de documentos PDF, Word, Excel
  [Habilitada]

✓ Calendar Integration
  Gestión de calendarios y programación de eventos
  [Deshabilitada]
```

**Requisitos Funcionales:**
- Por defecto: colapsado
- Al hacer clic en el contenedor: expandir suavemente (animación fade-in)
- Al volver a hacer clic: contraer suavemente (fade-out)
- El contenido debe aparecer/desaparecer realmente, no solo cambiar icono o color
- Cada agente tiene su propio estado de expansión (pueden estar abiertos/cerrados independientemente)
- Debe funcionar en tema claro y oscuro sin pérdida de legibilidad
- Debe adaptarse a escritorio (expandible en línea) y móvil (posible que se adapte a cards)
- Transición suave: `transition-all 200ms ease-in-out`
- Permite identificar claramente qué skills utiliza cada agente

**Datos Ficticios:**
Incluir mínimo 2-3 skills por agente, con estados variados (habilitadas/deshabilitadas):
- DataBot: "Web Browsing" (habilitada), "Document Analysis" (habilitada), "Data Export" (deshabilitada)
- WebScraperAI: "Web Browsing" (habilitada), "Screenshot Capture" (habilitada)
- AnalysisBot: "Document Analysis" (habilitada), "Data Visualization" (habilitada), "Report Generation" (deshabilitada)

#### Acciones por Agente
- **Configurar:** Abre formulario para editar parámetros
- **Eliminar:** Solicita confirmación

#### Modal de Configuración
Permite editar:
- **System Prompt:** Campo de texto multilinea para instrucciones del agente
- **Nombre:** Alias del agente
- **Skills:** Checkboxes para habilitar/deshabilitar
- **Parámetros técnicos:** Ficticios pero coherentes

Acciones:
- **Guardar:** Persiste cambios en localStorage
- **Cancelar:** Cierra sin guardar
- **Feedback visual:** Confirmación de guardado exitoso

---

### 4.4 Skills (Capacidades)

**Propósito:** Catálogo de habilidades que pueden asignarse a agentes.

#### Definición de Skill
Una skill es una capacidad especializada que un agente puede ejecutar. Ejemplos:
- Navegación web (web browsing)
- Análisis de documentos (document analysis)
- Gestión de calendarios (calendar management)
- Generación de código (code generation)
- Análisis de datos (data analysis)

#### Catálogo
Tabla o grid con:

| Columna | Contenido |
|---------|-----------|
| **Nombre** | Nombre de la skill |
| **Descripción** | Resumen breve de funcionalidad |
| **Agentes Usando** | Número de agentes que utilizan esta skill |

#### Acciones por Skill
- **Ver Detalle:** Abre modal informativo
- **Eliminar:** Solicita confirmación (si no hay agentes dependientes)

#### Modal de Detalle
Muestra:
- Nombre completo
- Descripción detallada
- Parámetros técnicos
- Lista de agentes que utilizan esta skill
- Fecha de creación/última actualización (ficticios)

---

### 4.5 Contrataciones de Agentes

**Propósito:** Registrar y administrar contratos entre clientes y agentes.

#### Tabla de Contratos
Muestra contratos activos y pasados:

| Columna | Contenido |
|---------|-----------|
| **Cliente** | Nombre de la organización/usuario contratante |
| **Agente** | Agente contratado |
| **Skills** | Skills incluidas en el contrato |
| **Fecha Inicio** | Cuándo comienza el contrato |
| **Fecha Fin** | Cuándo termina (puede estar vacío si está activo) |
| **Importe Total** | Monto total pagado/contratado |

#### Acciones
- **Ver Detalle:** Abre modal con información completa

#### Modal de Detalle del Contrato
Muestra:
- Información del cliente
- Información del agente contratado
- Fecha de inicio y fin
- Skills incluidas con especificaciones
- **Desglose de Precios:**
  - Precio base del agente
  - Precio por skill (individual)
  - Descuentos aplicados
  - Impuestos (ficticios)
  - **Total:**
- Historial de pagos (ficticios)
- Estado del contrato (Activo, Vencido, Cancelado)

---

### 4.6 Log de Errores

**Propósito:** Registrar y administrar errores operativos de la plataforma.

#### Tabla de Errores
Presenta errores con información clave:

| Columna | Contenido |
|---------|-----------|
| **Timestamp** | Fecha y hora del error |
| **Agente** | Agente involucrado |
| **Tipo** | Crítico, Advertencia, Información |
| **Descripción** | Resumen breve del problema |
| **Estado** | Pendiente, Resuelto |

#### Tipos de Error
- **Crítico (🔴):** Fallos que impiden operación normal (rojo)
- **Advertencia (🟡):** Problemas que degradan rendimiento (amarillo)
- **Información (🔵):** Eventos informativos (azul)

#### Acciones por Error
- **Ver Detalle:** Abre modal con stack trace y más información
- **Marcar como Resuelto:** Cambia estado a resuelto, mantiene registro, actualiza badge visualmente

#### Modal de Detalle
Muestra:
- Timestamp completo
- Agente involucrado
- Tipo de error
- Descripción completa
- **Stack trace** (ficticio pero coherente):
  - Ruta del error
  - Función donde ocurrió
  - Línea de código (aproximada)
  - Mensaje de error detallado
- Estado actual
- Botón "Marcar como Resuelto" (si aún está pendiente)

#### Errores Resueltos

**Cambio de Estado:**
- Cuando un error se marca como resuelto:
  - El estado en la tabla cambia de "Pendiente" a "Resuelto"
  - Se muestra badge verde con texto: "✓ Resuelto"
  - El cambio es inmediato (sin recargar página)
  - El registro se mantiene en la tabla (no se elimina)
  - La acción "Marcar como Resuelto" desaparece del menú (no se puede re-marcar)
  - Se muestra un feedback visual (toast o confirmación breve)

**Persistencia:**
- El estado resuelto se guarda en **localStorage** con key: `agenthub-error-{id}-resolved`
- Al recargar la página, el estado se recupera correctamente
- El badge verde se muestra nuevamente en la fila correspondiente

**Visualización en Historial:**
- Los errores resueltos permanecen completamente visibles en el listado
- Se pueden consultar detalles y stack trace igual que un error pendiente
- Pueden filtrarse por estado (opcional: "Mostrar resueltos" / "Ocultar resueltos")
- Color de fila: sin cambios (mantiene legibilidad)
- Badge de estado es el único indicador visual del cambio

---

## 5. Comportamientos Generales de la Interfaz

### Navegación
- **Sidebar:** Panel de navegación lateral izquierdo (collapsible en mobile)
  - Contiene 6 secciones principales: Dashboard, Usuarios, Agentes, Skills, Contrataciones, Errores
  - Resalta sección activa visualmente
  - Accesible mediante teclado
  
- **Topbar:** Barra superior con:
  - Nombre/logo de la plataforma
  - Selector de tema (Light/Dark)
  - Menú de usuario (opcional)

### Dropdowns
- Se cierran automáticamente al:
  - Hacer clic fuera del elemento
  - Seleccionar una opción
  - Presionar Escape
- Solo un dropdown abierto a la vez
- Animación suave de entrada/salida
- Accesibles con teclado (Arrow Up/Down, Enter)

### Modales
- Overlay oscuro detrás del modal (backdrop)
- Se cierran mediante:
  - Botón de cierre (X) en la esquina
  - Clic en el backdrop
  - Tecla Escape
- Focus atrapado dentro del modal mientras está abierto
- Animación de fade-in/fade-out

### Confirmaciones
- Modal de confirmación antes de cualquier eliminación
- Texto claro y advertencia visual
- Botones claramente marcados (Cancelar / Confirmar)
- El botón destructivo cambia de estilo

### Feedback Visual
- Mensajes de éxito después de guardar (toast o modal breve)
- Indicadores de carga (spinners) durante operaciones
- Cambios de color de inputs en focus
- Hover estados en botones y filas de tabla

### Persistencia
- Cambios se guardan en **localStorage** con claves estructuradas
- Preferencia de tema persiste entre sesiones
- Datos modificados (System Prompts, errores resueltos) se recuperan al recargar
- Registros "eliminados" se marcan como eliminados sin borrar realmente

---

## 6. Comportamientos Responsive

### Breakpoints
- **Desktop:** 1280px y superior
- **Tablet:** 768px a 1279px
- **Mobile:** Menos de 768px

### Comportamiento por Tamaño

#### Desktop (1280px+)
- Sidebar siempre visible (256px ancho)
- Layouts multi-columna
- Tablas con scroll horizontal disponible
- Modales centrados en pantalla

#### Tablet (768px - 1279px)
- Sidebar colapsable (modo icono-solamente, 64px)
- Layouts de 2 columnas
- Tablas condensadas
- Modales con padding reducido

#### Mobile (< 768px)
- Navegación en drawer off-canvas (oculta por defecto)
- Menú hamburguesa para abrir/cerrar
- Layouts de 1 columna
- Tablas horizontales scrollables
- Modales full-screen con padding inferior

### Elementos Específicos

**Tarjetas de KPI:**
- Desktop: 4 columnas
- Tablet: 2 columnas
- Mobile: 1 columna (stack vertical)

**Tablas:**
- Desktop: Tabla horizontal estándar
- Tablet: Tabla condensada con menos columnas
- Mobile: Tarjetas apiladas verticales con información de columna como etiquetas

**Formularios:**
- Desktop: Campos lado a lado cuando sea posible
- Mobile: Campos full-width apilados

**Gráficos:**
- Desktop: Tamaño completo
- Mobile: Responsive con altura limitada

---

## 7. Requisitos de Accesibilidad

### Navegación por Teclado
- Todos los elementos interactivos deben ser accesibles con Tab
- Orden lógico de tabulación (top-left → bottom-right)
- Shift+Tab para navegación reversa
- Enter/Space para activar botones y checkboxes
- Arrow keys en dropdowns y menus

### Estados Focus Visibles
- Outline o ring visible alrededor de elementos focused
- Contraste adecuado (mínimo 3:1 con fondo)
- Color de focus consistente (Indigo/Azul)

### Contraste
- Texto en fondo: mínimo 7:1 (WCAG AAA)
- Elementos interactivos: mínimo 4.5:1 (WCAG AA)
- Iconos de acción: contraste suficiente para distinguirse

### Etiquetas y Descripciones
- Todos los inputs tienen labels asociados
- Botones tienen texto descriptivo o aria-label
- Iconos tienen títulos o descripciones alternativas
- Tablas tienen headers semánticos

### Controles Accesibles
- Checkboxes y radios con estados visibles
- Inputs con estados de validación claros
- Buttons con estados disabled claramente identificados
- Modales con rol="dialog" y aria-labelledby

---

## 8. Sistema de Persistencia (localStorage)

### Claves Implementadas
Respetando la estructura observada en el código:

```
agenthub_theme: "light" | "dark"           // Preferencia de tema
agenthub_users: JSON                        // Datos de usuarios (con cambios)
agenthub_agents: JSON                       // Datos de agentes (con cambios)
agenthub_skills: JSON                       // Datos de skills
agenthub_contracts: JSON                    // Datos de contratos
agenthub_errors: JSON                       // Registro de errores
agenthub_system_prompts: JSON               // System prompts editados
```

**Nota:** Las claves específicas exactas no han sido verificadas en el código fuente; esta especificación documenta el comportamiento esperado sin inventar estructuras internas no confirmadas.

---

## 9. Criterios de Aceptación

### Verificación de Funcionalidad

#### Dashboard
- [ ] Muestra 4 KPIs con valores ficticios coherentes
- [ ] Gráfico de actividad renderiza correctamente
- [ ] **Tabla de actividad muestra mínimo 10 filas de datos ficticios coherentes**
  - [ ] Columnas: Timestamp, Agente, Acción, Duración, Estado
  - [ ] Encabezados en uppercase y semibold
  - [ ] Badges de estado diferenciados por color (Éxito verde, Fallo rojo, En progreso azul)
  - [ ] Duración en formato monoespaciado (ej. "2.5s", "1m 30s")
  - [ ] Timestamps claros y legibles (ej. "Nov 20, 2024 14:30")
  - [ ] Filas separadas visualmente (bordes o fondos alternados)
  - [ ] Se visualiza correctamente en ambos temas (Light y Dark Mode)
  - [ ] Responsive: en mobile se adapta sin desbordes
- [ ] Los datos persisten al recargar la página

#### Gestión de Usuarios
- [ ] Tabla carga y muestra al menos 3 usuarios ficticios
- [ ] Botón "Ver Detalle" abre modal con información completa
- [ ] Botón "Eliminar" solicita confirmación
- [ ] Los cambios persisten en localStorage

#### Gestión de Agentes
- [ ] Lista muestra agentes con estado (Activo/Inactivo/Fallando)
- [ ] **Skills colapsables funcionan correctamente:**
  - [ ] Colapsados por defecto (icono ▼ / ▶ visible)
  - [ ] Al expandir muestra lista de skills con nombre, descripción y estado
  - [ ] Cada skill muestra: nombre (semibold), descripción (pequeña), badge de estado (Habilitada/Deshabilitada)
  - [ ] El contenido aparece/desaparece realmente (no solo cambia icono)
  - [ ] Transición suave entre estados (fade-in/fade-out 200ms)
  - [ ] Cada agente expande/contrae independientemente
  - [ ] Funciona correctamente en tema Light y Dark
  - [ ] Se adapta a móvil sin problemas
  - [ ] Mínimo 2-3 skills por agente con estados variados
- [ ] Botón "Configurar" abre modal de edición
- [ ] System Prompt editable y guardable
- [ ] Cambios persisten en localStorage

#### Skills
- [ ] Catálogo muestra al menos 5 skills ficticias
- [ ] Cada skill muestra número de agentes usando
- [ ] "Ver Detalle" abre información completa
- [ ] "Eliminar" solo se permite si no hay agentes dependientes

#### Contrataciones
- [ ] Tabla muestra contratos activos y pasados
- [ ] "Ver Detalle" abre desglose de precios
- [ ] Información de cliente, agente y skills visible
- [ ] Cálculo de totales coherente

#### Log de Errores
- [ ] Muestra errores con tipos diferenciados (crítico, advertencia, info)
- [ ] "Ver Detalle" muestra stack trace ficticio
- [ ] **"Marcar como Resuelto" funciona correctamente:**
  - [ ] Botón disponible en modal de detalle (si error está pendiente)
  - [ ] Al hacer clic, el estado cambia inmediatamente de "Pendiente" a "Resuelto"
  - [ ] Aparece badge verde "✓ Resuelto" en la tabla
  - [ ] El error permanece visible en el historial (no se elimina)
  - [ ] Feedback visual confirma la acción (toast o mensaje breve)
  - [ ] El botón desaparece para errores ya resueltos
  - [ ] El estado persiste en localStorage (key: `agenthub-error-{id}-resolved`)
  - [ ] Al recargar, el estado resuelto se mantiene
  - [ ] Se puede consultar detalle y stack trace de errores resueltos
- [ ] Errores resueltos permanecen en historial

### Verificación de Interfaz

#### Navegación
- [ ] Sidebar navega entre las 6 secciones
- [ ] Sección activa se resalta visualmente
- [ ] Topbar muestra selector de tema funcional

#### Temas
- [ ] Light Mode usa paleta clara definida
- [ ] Dark Mode usa paleta oscura definida
- [ ] Clase `dark` cambia los colores correctamente
- [ ] Preferencia persiste entre sesiones

#### Modales y Dropdowns
- [ ] Modales se abren y cierran suavemente
- [ ] Clic en backdrop cierra modal
- [ ] Tecla Escape cierra modal
- [ ] Dropdowns se cierran al seleccionar
- [ ] Solo un dropdown abierto a la vez

#### Responsive
- [ ] Desktop (1280px+): Layout correcto con sidebar visible
- [ ] Tablet (768-1279px): Sidebar colapsable
- [ ] Mobile (<768px): Drawer off-canvas funcional
- [ ] Tablas adaptables en mobile
- [ ] Modales readaptables

#### Accesibilidad
- [ ] Navegación completa con Tab
- [ ] Focus visible en todos los elementos
- [ ] Contraste adecuado en light y dark mode
- [ ] Modales atrapan focus
- [ ] Etiquetas en inputs accesibles

#### Calidad
- [ ] Sin errores en la consola del navegador
- [ ] Consistencia visual entre las 6 secciones
- [ ] Tipografía correcta (Geist para UI, JetBrains Mono para código)
- [ ] Iconografía consistente
- [ ] Animaciones suaves sin saltos

---

## 10. Stack Visual Detallado

### Componentes Comunes

#### Buttons
**Primary (Acciones principales):**
- Fondo: Indigo 600 (Light: `#4f46e5`, Dark: `#c0c1ff`)
- Texto: Blanco (Light), Indigo muy oscuro (Dark)
- Hover: Indigo más oscuro
- Border-radius: `0.5rem`
- Padding: `0.5rem 1rem`

**Secondary (Acciones secundarias):**
- Fondo: Transparente
- Borde: 1px sólido (Light: `#e2e8f0`, Dark: `#2d3449`)
- Texto: Texto principal
- Hover: Fondo ligeramente tintado

**Destructive (Eliminar):**
- Fondo: Rose/Red con baja opacidad
- Texto: Rose/Red intenso
- Borde: Rose/Red sutil
- Hover: Más intenso

#### Inputs
- Altura: `2.5rem` (40px)
- Padding: `0.75rem`
- Border-radius: `0.5rem`
- Borde: 1px sólido (default)
- Focus: Borde Indigo + ring sutil

#### Status Badges
- Border-radius: `9999px` (pill)
- Padding: `0.25rem 0.625rem`
- Altura: `1.5rem` (24px)
- Font: `label-sm` (JetBrains Mono)

**Estados:**
- Activo: Fondo verde claro, texto verde oscuro
- Advertencia: Fondo amarillo claro, texto amarillo oscuro
- Crítico/Error: Fondo rojo claro, texto rojo oscuro
- Neutral: Fondo gris claro, texto gris oscuro

#### Cards
- Borde: 1px sólido (Light: `#e2e8f0`, Dark: `#2d3449`)
- Border-radius: `1rem` (16px)
- Padding: `1rem` a `1.5rem`
- Fondo: Superficie principal

#### Tablas
- Encabezado: Fondo superficie secundaria, texto uppercase, font `label-sm`
- Filas: Borde inferior sutil
- Hover: Fondo ligeramente destacado
- Densidad: Padding vertical mínimo para escaneo rápido

---

## 11. Estado de Implementación y Limitaciones

### ✅ Verificado e Implementado
- Estructura base HTML5 accesible
- Paleta de colores Light Mode y Dark Mode definida en referencias
- Tipografía Geist y JetBrains Mono via CDN
- Tailwind CSS v4 via CDN
- Sistema de temas (Light/Dark) con localStorage
- Componentes responsive con breakpoints
- Navegación entre 6 secciones
- Modales y dropdowns funcionales
- Acceso a datos ficticios
- Persistencia básica en localStorage

### ⚠️ Pendiente de Verificación en Implementación
- Gráfico de actividad semanal (tecnología específica no determinada)
- Detalles exactos de stack trace en modal de errores
- Estructura exacta de JSON en localStorage
- Comportamiento de animaciones específicas
- Validación de formularios
- Mensajes de feedback (toast/snackbar)
- Iconografía específica (SVG/Icon set)

### ❌ No Verificado por Restricciones de Acceso
- Código JavaScript completo (posible exclusión por política de contenido)
- Archivos CSS personalizados
- Configuración específica de servidor
- Detalles de implementación de skills avanzadas

### 📋 Supuestos y Decisiones de Diseño
- **Datos ficticios:** Se asumen valores realistas pero no conectados a datos reales
- **Sin backend:** Toda la lógica es cliente-side, localStorage es la única persistencia
- **Sin APIs:** No hay integración con servicios externos
- **Accesibilidad:** Se asumen estándares WCAG 2.1 AA como mínimo
- **Browsers soportados:** Navegadores modernos con ES6+ nativo (Chrome, Firefox, Safari, Edge)

---

## 12. Notas Finales

Esta especificación funcional define los requisitos de **AgentHub** como plataforma SaaS de gestión de agentes de IA. El documento sirve como referencia para desarrollo, diseño y validación del producto.

**Próximos pasos recomendados:**
1. Revisar la implementación actual contra esta especificación
2. Priorizar funcionalidades faltantes
3. Validar accesibilidad con auditorías automatizadas
4. Realizar pruebas de usabilidad con usuarios reales
5. Documentar cualquier desviación deliberada de esta especificación

---

**Especificación completada:** Noviembre 2024
