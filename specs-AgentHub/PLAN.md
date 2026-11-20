# Plan de Trabajo: Prototipo Frontend de AgentHub

**Documento:** Plan de Implementación  
**Fecha:** Noviembre 2024  
**Propósito:** Definir un plan práctico y secuencial para completar el prototipo frontend de AgentHub

---

## Visión General

Este plan organiza el desarrollo del prototipo frontend de AgentHub en **cinco fases secuenciales**, priorizando:

1. **Excelencia visual:** Diseño moderno, profesional y coherente
2. **Cumplimiento funcional:** Todos los requisitos de `spec.md`
3. **Simplicidad:** Implementación clara sin complejidad innecesaria

El plan utiliza **HTML5**, **Tailwind CSS v4** (CDN), y **JavaScript ES6+ vanilla** sin frameworks adicionales.

---

## Fase 1: Diseño General

### Objetivo
Establecer una base visual sólida y coherente para toda la aplicación, unificando componentes, tipografía, colores y espaciados según la identidad definida en `spec.md`.

### Tareas Principales

#### 1.1 Estructura Base y Layout
- [ ] Crear estructura HTML5 semántica con meta tags y accesibilidad
- [ ] Configurar Tailwind CSS v4 mediante CDN
- [ ] Importar fuentes tipográficas (Geist, JetBrains Mono)
- [ ] Crear layout principal: Sidebar + Topbar + Contenido
- [ ] Implementar sistema de navegación por secciones (6 vistas)

#### 1.2 Sidebar
- [ ] Diseñar sidebar con 6 opciones de navegación (Dashboard, Usuarios, Agentes, Skills, Contrataciones, Errores)
- [ ] Implementar resaltado de sección activa
- [ ] Crear indicador visual de navegación actual
- [ ] Hacer collapsible en mobile (drawer off-canvas)
- [ ] Verificar accesibilidad (teclado, focus)

#### 1.3 Topbar
- [ ] Crear barra superior con logo/nombre de plataforma
- [ ] Implementar selector Light/Dark Mode
- [ ] Guardar preferencia en localStorage
- [ ] Aplicar tema elegido (clase `dark` en raíz)
- [ ] Verificar que ambos temas sean legibles

#### 1.4 Paleta de Colores y Temas
- [ ] Configurar variables CSS o Tailwind para colores Light Mode
  - Canvas, superficies, bordes, texto, acentos, estados (éxito/advertencia/error)
- [ ] Configurar variables CSS o Tailwind para colores Dark Mode
  - Mismo conjunto con valores oscuros
- [ ] Verificar contraste WCAG AAA para textos (Light), AA para interactivos
- [ ] Probar ambos temas en luz clara y oscura (físicamente si es posible)

#### 1.5 Componentes Reutilizables
- [ ] Diseñar y codificar botones (Primary, Secondary, Destructive)
- [ ] Diseñar y codificar inputs y textareas
- [ ] Diseñar y codificar status badges (Activo, Inactivo, Fallando, Resuelto)
- [ ] Diseñar y codificar tarjetas genéricas
- [ ] Diseñar y codificar tablas (encabezados, filas, hover)
- [ ] Crear componentes de modal/overlay genéricos
- [ ] Crear componentes de confirmación de eliminación

#### 1.6 Responsive Design
- [ ] Verificar layout en Desktop (1280px+): sidebar visible, multi-columna
- [ ] Verificar layout en Tablet (768-1279px): sidebar colapsable, 2 columnas
- [ ] Verificar layout en Mobile (<768px): drawer, single-column
- [ ] Probar en dispositivos reales o devtools
- [ ] Ajustar tipografía, espaciado y componentes por breakpoint

#### 1.7 Animaciones y Transiciones
- [ ] Suavizar transiciones de tema (fade in/out)
- [ ] Agregar animaciones a dropdown, modal (entrada/salida)
- [ ] Implementar hover states visuales en botones y filas
- [ ] Comprobar que las animaciones sean fluidas (60fps, sin saltos)

#### 1.8 Verificación General
- [ ] No hay errores en consola
- [ ] Coherencia visual entre componentes
- [ ] Tipografía correcta (Geist, JetBrains Mono)
- [ ] Espaciado consistente
- [ ] Colores coherentes con spec.md

### Estado
**Pendiente**

---

## Fase 2: Dashboard

### Objetivo
Implementar la pantalla principal del dashboard con métricas clave, gráfico de actividad semanal y tabla de eventos recientes.

### Tareas Principales

#### 2.1 Tarjetas de KPI
- [ ] Crear 4 tarjetas con métricas:
  - Ingresos Totales del Mes ($45,320.00)
  - Pérdidas por Descuentos (-$2,150.00)
  - Agentes Activos (12/15)
  - Agentes Fallando (2)
- [ ] Usar iconografía SVG o Unicode para cada métrica
- [ ] Mostrar valor principal + indicador de tendencia (opcional)
- [ ] Aplicar espaciado y alineación responsiva (4 columnas desktop, 2 tablet, 1 mobile)
- [ ] Usar status colors según estado (rojo para fallando)

#### 2.2 Gráfico de Actividad Semanal
- [ ] Crear datos ficticios de actividad últimos 7 días (Mon-Sun)
- [ ] Renderizar gráfico de barras o línea (sin libería externa: canvas o SVG simple)
- [ ] Mostrar eje X (días), eje Y (número de ejecuciones)
- [ ] Hacer responsive (escala según ancho)
- [ ] Agregar tooltip/hover con valor exacto

#### 2.3 Tabla de Actividad Reciente
- [ ] Crear tabla con columnas: Timestamp, Agente, Acción, Duración, Estado
- [ ] Generar datos ficticios coherentes (últimas 10 actividades)
- [ ] Aplicar estilos de tabla: encabezado, filas, hover
- [ ] Implementar scroll horizontal en mobile si es necesario
- [ ] Agregar badges de estado (éxito, fallo, en progreso)
- [ ] Hacer clickeable para ver detalle (opcional, no especificado)

#### 2.4 Datos Ficticios
- [ ] Generar estructura de datos JSON en JavaScript
- [ ] Cargar datos en memoria al iniciar aplicación
- [ ] Asegurar que valores sean coherentes (totales, conteos, fechas)
- [ ] Permitir reset manual de datos

#### 2.5 Verificación del Dashboard
- [ ] Las 4 tarjetas muestran valores correctos
- [ ] Gráfico renderiza sin errores
- [ ] Tabla es legible y bien espaciada
- [ ] Responsive en todos los tamaños
- [ ] Sin errores en consola

### Estado
**Pendiente**

---

## Fase 3: Secciones de Gestión

### Objetivo
Implementar las cuatro secciones de gestión (Usuarios, Agentes, Skills, Contrataciones) con tablas, detalles modales y acciones completas.

### Tareas Principales

#### 3.1 Gestión de Usuarios
- [ ] Crear tabla con columnas: Nombre, Email, Plan, Estado
- [ ] Generar datos ficticios (mínimo 5 usuarios)
- [ ] Implementar acciones por fila:
  - [ ] Botón "Ver Detalle" → abre modal
  - [ ] Botón "Eliminar" → solicita confirmación
- [ ] Modal de Detalle muestra:
  - [ ] Nombre, Email, Plan, Estado
  - [ ] Fecha de registro
  - [ ] Información ficticia de cuenta
  - [ ] Botones: Editar, Desactivar, Eliminar
- [ ] Modal de Confirmación (para eliminar)
  - [ ] Pregunta clara en rojo
  - [ ] Botones: Cancelar, Confirmar Eliminación
  - [ ] Se cierra con Escape o clic en backdrop
- [ ] Persistencia: guardar cambios en localStorage
- [ ] Verificar responsividad (tabla en mobile se adapta)

#### 3.2 Gestión de Agentes
- [ ] Crear listado con columnas: Nombre, Propietario, Estado, Skills
- [ ] Generar datos ficticios (mínimo 5 agentes)
- [ ] Implementar skills colapsables:
  - [ ] Por defecto: colapsados
  - [ ] Al expandir: mostrar lista de skills con nombre y versión
  - [ ] Solo un agente con skills expandidas a la vez (opcional)
- [ ] Implementar acciones por agente:
  - [ ] Botón "Configurar" → abre modal de edición
  - [ ] Botón "Eliminar" → solicita confirmación
- [ ] Modal de Configuración permite editar:
  - [ ] System Prompt (campo de texto multilinea)
  - [ ] Nombre del agente
  - [ ] Checkboxes para habilitar/deshabilitar skills
  - [ ] Parámetros técnicos ficticios
  - [ ] Botones: Guardar, Cancelar
- [ ] Guardar cambios de System Prompt en localStorage
- [ ] Mostrar feedback visual al guardar (toast o confirmación breve)
- [ ] Verificar responsividad

#### 3.3 Catálogo de Skills
- [ ] Crear tabla con columnas: Nombre, Descripción, Agentes Usando
- [ ] Generar datos ficticios (mínimo 5-6 skills):
  - Navegación Web
  - Análisis de Documentos
  - Gestión de Calendarios
  - Generación de Código
  - Análisis de Datos
  - Etc.
- [ ] Implementar acciones por skill:
  - [ ] Botón "Ver Detalle" → abre modal
  - [ ] Botón "Eliminar" → solicita confirmación (solo si no hay agentes dependientes)
- [ ] Modal de Detalle muestra:
  - [ ] Nombre y descripción detallada
  - [ ] Parámetros técnicos ficticios
  - [ ] Lista de agentes que usan esta skill
  - [ ] Fecha de creación/actualización (ficticios)
- [ ] Verificar responsividad

#### 3.4 Contrataciones de Agentes
- [ ] Crear tabla con columnas: Cliente, Agente, Skills, Fecha Inicio, Fecha Fin, Importe Total
- [ ] Generar datos ficticios (mínimo 5 contratos, activos y vencidos)
- [ ] Implementar acción:
  - [ ] Botón "Ver Detalle" → abre modal
- [ ] Modal de Detalle muestra:
  - [ ] Información del cliente
  - [ ] Información del agente contratado
  - [ ] Fechas de inicio y fin
  - [ ] Skills incluidas
  - [ ] **Desglose de Precios:**
    - Precio base del agente
    - Precio por skill (individual)
    - Descuentos aplicados
    - Impuestos ficticios
    - **Total calculado**
  - [ ] Historial de pagos (ficticios)
  - [ ] Estado del contrato
- [ ] Verificar que cálculos de precios sean coherentes
- [ ] Verificar responsividad

#### 3.5 Verificación General de Fase 3
- [ ] Las 4 secciones cargan sin errores
- [ ] Todas las tablas muestran datos correctos
- [ ] Modales de detalle funcionan
- [ ] Modales de confirmación funcionan
- [ ] Cambios persisten en localStorage
- [ ] Responsive en todos los tamaños
- [ ] Sin errores en consola

### Estado
**Pendiente**

---

## Fase 4: Log de Errores e Interacciones

### Objetivo
Implementar el log de errores con tipos diferenciados, detalles modales, acciones de resolución y verificar todas las interacciones de la aplicación (dropdowns, modales, confirmaciones, persistencia).

### Tareas Principales

#### 4.1 Log de Errores - Tabla
- [ ] Crear tabla con columnas: Timestamp, Agente, Tipo, Descripción, Estado
- [ ] Generar datos ficticios (mínimo 10 errores con tipos variados)
- [ ] Implementar tipos con colores diferenciados:
  - [ ] Crítico (rojo) - `#e11d48` (Light), `#f43f5e` (Dark)
  - [ ] Advertencia (amarillo) - `#d97706` (Light), `#f59e0b` (Dark)
  - [ ] Información (azul) - `#4f46e5` (Light), `#c0c1ff` (Dark)
- [ ] Estado mostrado con badges (Pendiente, Resuelto)
- [ ] Errores resueltos muestran indicador verde (✓)
- [ ] Implementar acciones por error:
  - [ ] Botón "Ver Detalle" → abre modal
  - [ ] Botón "Marcar como Resuelto" → cambia estado
- [ ] Permitir filtrado por estado (opcional, según spec)
- [ ] Verificar responsividad

#### 4.2 Log de Errores - Modal de Detalle
- [ ] Modal muestra:
  - [ ] Timestamp completo
  - [ ] Agente involucrado
  - [ ] Tipo de error (con color)
  - [ ] Descripción completa
  - [ ] **Stack trace ficticio pero coherente:**
    - Archivo/ruta del error
    - Función donde ocurrió
    - Número de línea
    - Mensaje de error detallado
  - [ ] Estado actual (Pendiente/Resuelto)
  - [ ] Botón para marcar como resuelto
- [ ] Stack trace formateado con monoespaciada (JetBrains Mono)
- [ ] Persistencia: cambios de estado se guardan en localStorage

#### 4.3 Interacciones Globales: Dropdowns
- [ ] Verificar que dropdowns se cierren al:
  - [ ] Hacer clic fuera
  - [ ] Seleccionar una opción
  - [ ] Presionar Escape
- [ ] Verificar que solo haya un dropdown abierto a la vez
- [ ] Verificar accesibilidad: Arrow Up/Down, Enter
- [ ] Probar en todas las secciones (opciones de acciones, selectores)

#### 4.4 Interacciones Globales: Modales
- [ ] Verificar que modales se cierren mediante:
  - [ ] Botón de cierre (X)
  - [ ] Clic en backdrop (overlay)
  - [ ] Tecla Escape
- [ ] Verificar que focus esté atrapado dentro del modal mientras está abierto
- [ ] Verificar animaciones de entrada/salida
- [ ] Probar en todas las secciones

#### 4.5 Interacciones Globales: Confirmaciones
- [ ] Verificar que antes de cualquier eliminación se solicite confirmación
- [ ] Verificar que el texto de advertencia sea claro (rojo)
- [ ] Verificar que el botón destructivo sea distinguible
- [ ] Verificar que se pueda cancelar
- [ ] Probar en todas las secciones (Usuarios, Agentes, Skills)

#### 4.6 Feedback Visual
- [ ] Implementar mensajes de éxito después de:
  - [ ] Guardar System Prompt de agente
  - [ ] Eliminar registro
  - [ ] Marcar error como resuelto
- [ ] Feedback puede ser toast, modal breve, o cambio visual duratorio
- [ ] Duración: 2-3 segundos
- [ ] Accesible visualmente en ambos temas

#### 4.7 Persistencia (localStorage)
- [ ] Verificar que se guarden:
  - [ ] Preferencia de tema (Light/Dark)
  - [ ] System Prompts editados (Agentes)
  - [ ] Estados de errores resueltos
  - [ ] Registros eliminados (marcados como eliminados, no borrados)
  - [ ] Cambios en datos de usuarios (si aplica)
- [ ] Verificar que al recargar la página se recuperen los cambios
- [ ] Verificar que localStorage no contenga datos sensibles o personales reales
- [ ] Documentar las claves de localStorage utilizadas

#### 4.8 Accesibilidad General
- [ ] Verificar navegación completa con Tab
- [ ] Verificar que focus sea visible en todos los elementos interactivos
- [ ] Verificar que orden de tabulación sea lógico (top-left → bottom-right)
- [ ] Verificar Shift+Tab para navegación reversa
- [ ] Verificar que inputs tengan labels accesibles
- [ ] Verificar que botones tengan texto descriptivo o aria-label
- [ ] Verificar que modales tengan rol="dialog"
- [ ] Verificar contraste en ambos temas (WCAG AAA para textos)

#### 4.9 Verificación General de Fase 4
- [ ] Log de errores cargue sin errores
- [ ] Todos los tipos de error se muestren con colores correctos
- [ ] Modales de detalle y confirmación funcionen
- [ ] Acciones "Marcar como Resuelto" funcione
- [ ] Dropdowns se cierren correctamente
- [ ] Persistencia en localStorage funcione
- [ ] Cambios persistan al recargar
- [ ] Sin errores en consola
- [ ] Navegación por teclado funcione en todas las secciones

### Estado
**Pendiente**

---

## Fase 5: Revisión Final

### Objetivo
Validar que la implementación completa cumpla con la especificación, presente excelencia visual en todos los tamaños y temas, y esté libre de errores.

### Tareas Principales

#### 5.1 Revisión de las Seis Secciones
- [ ] **Dashboard**
  - [ ] 4 KPIs mostrados correctamente
  - [ ] Gráfico renderizado sin errores
  - [ ] Tabla legible y bien espaciada
  - [ ] Datos ficticios coherentes
- [ ] **Gestión de Usuarios**
  - [ ] Tabla cargada
  - [ ] Modales de detalle y confirmación funcionan
  - [ ] Cambios persistidos
- [ ] **Gestión de Agentes**
  - [ ] Lista de agentes cargada
  - [ ] Skills colapsables funcionan
  - [ ] Modal de configuración permite editar System Prompt
  - [ ] Cambios persistidos
- [ ] **Skills**
  - [ ] Catálogo cargado
  - [ ] Modal de detalle funciona
  - [ ] Número de agentes usando correcto
- [ ] **Contrataciones**
  - [ ] Tabla cargada
  - [ ] Modal con desglose de precios funciona
  - [ ] Cálculos coherentes
- [ ] **Log de Errores**
  - [ ] Tabla cargada con tipos de error
  - [ ] Modal de detalle con stack trace funciona
  - [ ] Cambio de estado (Marcar como Resuelto) funciona
  - [ ] Cambios persistidos

#### 5.2 Revisión de Requisitos Funcionales
- [ ] Todos los requisitos de `spec.md` están implementados
- [ ] No hay funcionalidades adicionales no solicitadas
- [ ] Comportamientos generales cumplidos:
  - [ ] Navegación entre secciones funciona
  - [ ] Sidebar visible en desktop, collapsable en mobile
  - [ ] Topbar con selector de tema
  - [ ] Dropdowns se cierran correctamente
  - [ ] Modales se cierran con Escape, backdrop, botón X
  - [ ] Confirmaciones antes de eliminar
  - [ ] Feedback visual después de acciones
  - [ ] localStorage persiste cambios

#### 5.3 Revisión de Coherencia Visual
- [ ] Colores consistentes con paleta Light Mode
- [ ] Colores consistentes con paleta Dark Mode
- [ ] Tipografía correcta (Geist para UI, JetBrains Mono para código)
- [ ] Espaciado consistente en todas las secciones
- [ ] Radiuses consistentes (botones 0.5rem, tarjetas 1rem, modales 1.5rem)
- [ ] Botones y componentes reutilizables sin variaciones inconsistentes
- [ ] Iconografía consistente
- [ ] Alineación y jerarquía visual clara

#### 5.4 Revisión de Light Mode
- [ ] Canvas de fondo: `#faf8ff`
- [ ] Superficies principales: `#ffffff`
- [ ] Bordes: `#e2e8f0`
- [ ] Texto principal: `#131b2e`
- [ ] Texto secundario: `#334155`
- [ ] Acento primario: `#4f46e5`
- [ ] Badges: colores correctos (éxito, advertencia, error)
- [ ] Contraste suficiente (WCAG AAA para textos, AA para elementos)
- [ ] Legibilidad en luz clara

#### 5.5 Revisión de Dark Mode
- [ ] Canvas de fondo: `#0b1326`
- [ ] Superficies principales: `#131b2e`
- [ ] Superficies elevadas: `#1e293b`
- [ ] Bordes: `#2d3449`
- [ ] Texto principal: `#dae2fd`
- [ ] Texto secundario: `#908fa0`
- [ ] Acento primario: `#c0c1ff`
- [ ] Badges: colores correctos
- [ ] Contraste suficiente
- [ ] Legibilidad en luz oscura
- [ ] Transición suave al cambiar de tema

#### 5.6 Revisión de Responsive Design
- [ ] **Desktop (1280px+)**
  - [ ] Sidebar visible a la izquierda
  - [ ] Contenido ocupa el espacio disponible
  - [ ] Tablas sin scroll innecesario
  - [ ] Modales centrados
  - [ ] 4 columnas de tarjetas en dashboard
- [ ] **Tablet (768-1279px)**
  - [ ] Sidebar colapsable a icono-only (64px)
  - [ ] Contenido se ajusta
  - [ ] 2 columnas en dashboard
  - [ ] Tablas condensadas
  - [ ] Modales con padding reducido
- [ ] **Mobile (<768px)**
  - [ ] Drawer off-canvas para navegación
  - [ ] Menú hamburguesa visible
  - [ ] 1 columna en dashboard (stack vertical)
  - [ ] Tablas como tarjetas apiladas verticales
  - [ ] Modales full-screen o casi full-screen
  - [ ] Touch-friendly (tamaños de botones, espaciado)
- [ ] Probar en DevTools (Chrome, Firefox) con distintos tamaños
- [ ] Probar en dispositivos reales si es posible

#### 5.7 Revisión de Accesibilidad
- [ ] Sin errores detectados por axe DevTools o similar
- [ ] Navegación por teclado en todas las secciones
- [ ] Focus visible en elementos interactivos
- [ ] Orden de tabulación lógico
- [ ] Inputs tienen labels accesibles
- [ ] Botones tienen texto descriptivo
- [ ] Modales con rol="dialog" y aria-labelledby
- [ ] Colores no son el único medio de comunicar estado (también usar iconos, texto)

#### 5.8 Revisión de Calidad Técnica
- [ ] **Consola del navegador:** Sin errores, warnings mínimos
- [ ] **HTML:** Semántico, válido
- [ ] **CSS:** Consistente, sin duplicidades innecesarias
- [ ] **JavaScript:** Legible, funcional, sin funciones no utilizadas
- [ ] **Rendimiento:** Sin lag visible, transiciones suaves
- [ ] **Datos:** Ficticios pero coherentes y realistas
- [ ] **localStorage:** Claves bien nombradas, sin datos sensibles

#### 5.9 Corrección de Errores
- [ ] Revisar cada error/warning detectado
- [ ] Priorizar correcciones por impacto en UX/accesibilidad
- [ ] Máximo 2-3 intentos de corrección por error
- [ ] Documentar errores no corregibles con justificación

#### 5.10 Checklist Final
- [ ] ¿Funciona en Chrome, Firefox, Safari, Edge? (mínimo probar en 2)
- [ ] ¿Todas las 6 secciones funcionan correctamente?
- [ ] ¿Cambios persisten en localStorage?
- [ ] ¿Tema Light y Dark funcionan?
- [ ] ¿Responsive en 3 tamaños?
- [ ] ¿Sin errores en consola?
- [ ] ¿Visual coherente y profesional?
- [ ] ¿Especificación cumplida?

### Estado
**Pendiente**

---

## Reglas de Implementación

1. **Stack Obligatorio**
   - HTML5 semántico
   - Tailwind CSS v4 (CDN)
   - JavaScript ES6+ vanilla
   - Sin frameworks (React, Vue, Angular)
   - Sin librerías externas (excepto Tailwind y fuentes)

2. **Simplicidad**
   - Código legible y comprensible
   - Sin abstracciones innecesarias
   - Reutilizar componentes cuando sea posible
   - No refactorizar código existente no relacionado

3. **Funcionalidad**
   - Solo requisitos de `spec.md`
   - Sin funcionalidades adicionales
   - Datos ficticios pero coherentes
   - localStorage para persistencia

4. **Visión Visual**
   - Priorizar diseño profesional
   - Mantener coherencia visual
   - Respetar paleta de colores y tipografía
   - Verificar contraste y accesibilidad
   - Ambos temas (Light/Dark) siempre funcionales

5. **Validación**
   - No marcar tarea como "Completada" sin verificación
   - Probar en DevTools y si es posible dispositivos reales
   - Revisar consola para errores
   - Comprobar localStorage y persistencia

---

## Seguimiento y Control

### Por Fase
Cada fase debe alcanzar estado **Completada** solo cuando:
- Todas las tareas estén ejecutadas
- Se haya verificado cada tarea
- No haya errores críticos en consola
- El código cumpla con especificación

### Estados Posibles
- **Pendiente:** Aún no iniciada
- **En Progreso:** Actualmente se está trabajando
- **Completada:** Verificada y funcional
- **Bloqueada:** Impedimento detectado (documentar en observaciones)

### Métricas
- Tiempo estimado por fase: 1-2 horas (variable según complejidad)
- Prioridad: Fase 1 → Fase 2 → Fase 3 → Fase 4 → Fase 5
- No saltar fases

---

## Próximas Acciones

1. Revisar este plan con stakeholders
2. Comenzar por Fase 1: Diseño General
3. Registrar progreso en cada tarea
4. Ajustar plan si se encuentran bloqueadores
5. Documentar cualquier desviación deliberada
6. Al finalizar todas las fases, actualizar el estado del proyecto

---

**Documento de Plan completado:** Noviembre 2024
