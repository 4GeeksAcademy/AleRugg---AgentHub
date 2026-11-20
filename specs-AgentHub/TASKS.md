# Lista de Tareas: Prototipo Frontend de AgentHub

**Documento:** Tareas Concretas  
**Fecha:** Noviembre 2024  
**Propósito:** Lista detallada de tareas para completar el prototipo frontend

---

## 1. Diseño General

### Mejora de apariencia global
- [ ] Revisar layout general (Sidebar + Topbar + Contenido)
- [ ] Ajustar ancho máximo del contenido y márgenes
- [ ] Revisar espaciado entre secciones
- [ ] Verificar que el fondo sea coherente con la paleta

### Unificación de Sidebar y Topbar
- [ ] Revisar colores y bordes en Sidebar
- [ ] Asegurar que logo/nombre aparezca en Topbar
- [ ] Verificar que selector Light/Dark esté en Topbar
- [ ] Revisar que hover states sean consistentes
- [ ] Asegurar que navegación activa se resalte correctamente

### Perfeccionamiento de tarjetas
- [ ] Revisar border-radius (debe ser `1rem`)
- [ ] Verificar sombras y bordes (debe ser sutil)
- [ ] Ajustar padding interno (debe ser coherente)
- [ ] Revisar colores de fondo en ambos temas
- [ ] Comprobar que transiciones sean suaves

### Perfeccionamiento de tablas
- [ ] Revisar estilos de encabezado (fondo, tipografía)
- [ ] Ajustar altura de filas (mínimo 48px)
- [ ] Revisar hover states en filas
- [ ] Verificar alineación de texto en columnas
- [ ] Comprobar responsividad en móvil

### Perfeccionamiento de botones
- [ ] Revisar Primary: color, hover, padding
- [ ] Revisar Secondary: borde, color, hover
- [ ] Revisar Destructive: color rojo, hover
- [ ] Verificar tamaño (mínimo 44px altura para touch)
- [ ] Comprobar focus states (outline o ring)

### Perfeccionamiento de formularios
- [ ] Revisar estilos de inputs (borde, fondo, focus)
- [ ] Ajustar altura (mínimo 40px)
- [ ] Verificar labels accesibles
- [ ] Revisar textareas (System Prompt)
- [ ] Comprobar validación visual si aplica

### Perfeccionamiento de modales
- [ ] Revisar tamaño y posición (centrado)
- [ ] Ajustar padding interno
- [ ] Verificar botón de cierre (X)
- [ ] Revisar backdrop (overlay oscuro)
- [ ] Comprobar animaciones de entrada/salida

### Tipografía y estilos
- [ ] Verificar que Geist se carga correctamente
- [ ] Verificar que JetBrains Mono se carga correctamente
- [ ] Revisar tamaños de fuentes por nivel (títulos, cuerpo, etiquetas)
- [ ] Ajustar line-height para legibilidad
- [ ] Comprobar pesos de fuente (normal, semibold, bold)

### Colores Light Mode
- [ ] Canvas: `#faf8ff`
- [ ] Superficies: `#ffffff`
- [ ] Bordes: `#e2e8f0`
- [ ] Texto principal: `#131b2e`
- [ ] Texto secundario: `#334155`
- [ ] Acento primario: `#4f46e5`
- [ ] Éxito: `#059669`
- [ ] Advertencia: `#d97706`
- [ ] Error: `#e11d48`

### Colores Dark Mode
- [ ] Canvas: `#0b1326`
- [ ] Superficies principales: `#131b2e`
- [ ] Superficies elevadas: `#1e293b`
- [ ] Bordes: `#2d3449`
- [ ] Texto principal: `#dae2fd`
- [ ] Texto secundario: `#908fa0`
- [ ] Acento primario: `#c0c1ff`
- [ ] Éxito: `#10b981`
- [ ] Advertencia: `#f59e0b`
- [ ] Error: `#f43f5e`

### Responsive Desktop (1280px+)
- [ ] Sidebar siempre visible a la izquierda
- [ ] Contenido ocupa el espacio disponible
- [ ] Tablas sin scroll innecesario
- [ ] Modales centrados
- [ ] Grid de tarjetas: 4 columnas en Dashboard

### Responsive Tablet (768-1279px)
- [ ] Sidebar colapsable o comprimido a icono-only
- [ ] Contenido se ajusta al espacio
- [ ] Grid de tarjetas: 2 columnas en Dashboard
- [ ] Tablas condensadas
- [ ] Modales con padding reducido

### Responsive Mobile (<768px)
- [ ] Drawer off-canvas para navegación
- [ ] Menú hamburguesa visible
- [ ] Contenido full-width
- [ ] Grid de tarjetas: 1 columna (stack) en Dashboard
- [ ] Tablas convertidas a tarjetas apiladas verticales
- [ ] Modales full-screen o casi full-screen

---

## 2. Dashboard

### Tarjetas de KPI
- [x] Tarjeta 1 - Ingresos Totales del Mes
  - [x] Mostrar valor en moneda (ej. $45,320.00)
  - [x] Mostrar icono o indicador visual
  - [x] Aplicar espaciado correcto
  - [x] Verificar en ambos temas
- [x] Tarjeta 2 - Pérdidas por Descuentos
  - [x] Mostrar valor negativo (ej. -$2,150.00)
  - [x] Usar color rojo para pérdida
  - [x] Verificar contraste
- [x] Tarjeta 3 - Agentes Activos
  - [x] Mostrar contador (ej. 12/15)
  - [x] Mostrar porcentaje
  - [x] Usar color verde
- [x] Tarjeta 4 - Agentes Fallando
  - [x] Mostrar contador
  - [x] Usar color rojo para criticidad
  - [x] Verificar que destaque visualmente

### Gráfico de Actividad Semanal
- [x] Renderizar gráfico (barras o línea) sin libería externa
- [x] Mostrar últimos 7 días (Mon-Sun)
- [x] Mostrar eje X (días) y eje Y (actividad)
- [x] Usar datos ficticios coherentes
- [x] Hacer responsive (escalar según ancho)
- [x] Agregar tooltip/hover con valor exacto

### Tabla de Actividad Reciente
- [x] Mostrar columnas: Timestamp, Agente, Acción, Duración, Estado
- [x] Generar datos ficticios (últimas 10 actividades)
- [x] Aplicar estilos de tabla correctamente
- [x] Agregar badges de estado (éxito, fallo, en progreso)
- [x] Implementar scroll horizontal en mobile si es necesario
- [x] Verificar que filas sean clickeables para ver detalle (opcional)

---

## 3. Gestión de Usuarios

### Tabla de usuarios
- [x] Mostrar columnas: Nombre, Email, Plan, Estado
- [x] Generar datos ficticios (mínimo 5 usuarios)
- [x] Aplicar estilos de tabla correctamente
- [x] Implementar hover states en filas
- [x] Verificar responsividad

### Menú de acciones
- [x] Botón "Ver Detalle" funciona (abre modal)
- [x] Botón "Eliminar" funciona (solicita confirmación)
- [x] Botones alineados correctamente
- [x] Iconografía clara (opcional)

### Modal de detalle
- [x] Mostrar nombre del usuario
- [x] Mostrar email
- [x] Mostrar plan activo
- [x] Mostrar estado
- [x] Mostrar fecha de registro
- [x] Mostrar información ficticia de cuenta
- [x] Incluir botones: Editar (opcional), Desactivar, Eliminar
- [x] Cierre funciona (X, Escape, backdrop)

### Eliminación con confirmación
- [x] Modal de confirmación se abre
- [x] Pregunta clara y texto en rojo
- [x] Botones: Cancelar, Confirmar Eliminación
- [x] Botón destructivo visualmente distintivo
- [x] Se cierra al cancelar o tras confirmar

---

## 4. Gestión de Agentes

### Listado de agentes
- [x] Mostrar columnas/campos: Nombre, Propietario, Estado, Skills
- [x] Generar datos ficticios (mínimo 5 agentes)
- [x] Estados mostrados correctamente: Activo, Inactivo, Fallando
- [x] Colores diferenciados por estado
- [x] Verificar responsividad

### Despliegue de skills (Collapsible)
- [x] Skills colapsados por defecto
- [x] Icono de expansión (▼ / ▶) visible
- [x] Al expandir, mostrar lista de skills
- [x] Cada skill muestra: nombre y versión
- [x] Expandir solo una vez (opcional: solo un agente a la vez)
- [x] Colapsar al hacer clic nuevamente

### Edición del system prompt
- [x] Botón "Configurar" abre modal
- [x] Modal muestra campo System Prompt (textarea multilinea)
- [x] Campo System Prompt editable
- [x] Botones: Guardar, Cancelar
- [x] Guardar persiste en localStorage
- [x] Mostrar feedback visual (toast/mensaje)

### Eliminación con confirmación
- [x] Botón "Eliminar" abre confirmación
- [x] Modal de confirmación clara
- [x] Botones: Cancelar, Confirmar Eliminación
- [x] Cambio de estado se refleja en tabla

---

## 5. Catálogo de Skills

### Tabla de skills
- [x] Mostrar columnas: Nombre, Descripción, Agentes Usando
- [x] Generar datos ficticios (mínimo 5-6 skills)
- [x] Descripciones claras y concisas
- [x] Número de agentes mostrado correctamente
- [x] Verificar responsividad

### Significado de skill
- [x] Incluir explicación clara de qué es una skill
- [x] Mostrar en la sección o en un tooltip
- [x] Ejemplos de skills disponibles
- [x] Texto accesible y profesional

### Modal de detalle
- [x] Mostrar nombre de skill
- [x] Mostrar descripción detallada
- [x] Mostrar parámetros técnicos ficticios
- [x] Mostrar lista de agentes que usan esta skill
- [x] Mostrar fecha de creación/actualización
- [x] Cierre funciona correctamente

### Eliminación
- [x] Botón "Eliminar" abre confirmación
- [x] No permitir eliminar si hay agentes dependientes
- [x] Mostrar mensaje si es caso bloqueado
- [x] Confirmación clara si se permite eliminar

---

## 6. Contrataciones

### Tabla de contrataciones
- [x] Mostrar columnas: Cliente, Agente, Skills, Fecha Inicio, Fecha Fin, Importe Total
- [x] Generar datos ficticios (contratos activos y vencidos)
- [x] Datos coherentes (fechas, montos)
- [x] Verificar responsividad

### Skills contratadas
- [x] Mostrar skills incluidas en cada contrato
- [x] Mostrar precio individual por skill
- [x] Desglose claro y legible

### Modal de detalle
- [x] Información del cliente
- [x] Información del agente contratado
- [x] Fechas de inicio y fin
- [x] Skills incluidas con especificaciones
- [x] Desglose de precios:
  - [x] Precio base del agente
  - [x] Precio por skill (individual)
  - [x] Descuentos aplicados
  - [x] Impuestos ficticios
  - [x] **Total calculado**
- [x] Historial de pagos ficticios
- [x] Estado del contrato
- [x] Cierre funciona correctamente

---

## 7. Log de Errores

### Tabla de errores
- [x] Mostrar columnas: Timestamp, Agente, Tipo, Descripción, Estado
- [x] Generar datos ficticios (mínimo 10 errores)
- [x] Tipos de error diferenciados: Crítico, Advertencia, Información
- [x] Colores correctos: rojo, amarillo, azul/indigo
- [x] Estados mostrados: Pendiente, Resuelto
- [x] Errores resueltos muestran indicador verde (✓)
- [x] Verificar responsividad

### Niveles de gravedad
- [x] Crítico: color rojo, icono o badge rojo
- [x] Advertencia: color amarillo, icono o badge amarillo
- [x] Información: color azul/indigo, icono o badge azul
- [x] Colores coherentes en ambos temas

### Modal de detalle
- [x] Timestamp completo
- [x] Agente involucrado
- [x] Tipo de error (con color)
- [x] Descripción completa
- [x] Stack trace ficticio:
  - Archivo/ruta del error
  - Función donde ocurrió
  - Número de línea
  - Mensaje de error detallado
  - Formato: monoespaciada (JetBrains Mono)
- [x] Estado actual
- [x] Botón para marcar como resuelto
- [x] Cierre funciona correctamente

### Acción Marcar como Resuelto
- [x] Botón "Marcar como Resuelto" disponible
- [x] Cambio de estado se refleja en tabla
- [x] Error permanece en historial (no se elimina)
- [x] Indicador visual de error resuelto (verde, ✓)
- [x] Cambio se persiste en localStorage

---

## 8. Interacciones y Persistencia

### Dropdowns
- [x] Verificar que se cierren al hacer clic fuera
- [x] Verificar que se cierren al seleccionar opción
- [x] Verificar que se cierren al presionar Escape
- [x] Solo un dropdown abierto a la vez
- [x] Accesibilidad: Arrow Up/Down, Enter funciona
- [x] Probar en todas las secciones

### Modales
- [x] Verificar apertura suave (animación fade-in)
- [x] Verificar cierre con botón X
- [x] Verificar cierre con clic en backdrop
- [x] Verificar cierre con Escape
- [x] Focus atrapado dentro del modal
- [x] Cierre suave (animación fade-out)
- [x] Probar en todas las secciones

### Botones y confirmaciones
- [x] Botones Primary funcionan correctamente
- [x] Botones Secondary funcionan correctamente
- [x] Botones Destructive están visualmente distintivos
- [x] Confirmaciones aparecen antes de eliminar
- [x] Confirmaciones tienen opciones claras (Cancelar/Confirmar)
- [x] Acciones se ejecutan correctamente

### Persistencia en localStorage
- [x] Preferencia de tema (Light/Dark) se guarda
- [x] Preferencia de tema se recupera al recargar
- [x] System Prompts editados se guardan
- [x] System Prompts se recuperan al recargar
- [x] Estados de errores resueltos se guardan
- [x] Estados se recuperan al recargar
- [x] Registros eliminados se mantienen marcados
- [x] No hay datos sensibles en localStorage

### Tema seleccionado
- [x] Selector Light/Dark en Topbar funciona
- [x] Cambio de tema es inmediato (sin recargar)
- [x] Clase `dark` se aplica al elemento raíz
- [x] Todos los colores cambian correctamente
- [x] Preferencia persiste entre sesiones

---

## 9. Revisión Final

### Navegación entre secciones
- [x] Dashboard accesible desde Sidebar
- [x] Gestión de Usuarios accesible
- [x] Gestión de Agentes accesible
- [x] Catálogo de Skills accesible
- [x] Contrataciones accesible
- [x] Log de Errores accesible
- [x] Sección activa se resalta visualmente
- [x] Navegación funciona sin errores

### Requisitos funcionales de spec.md
- [x] Todas las 6 secciones implementadas
- [x] Todos los modales funcionan
- [x] Todos los botones funcionan
- [x] Todas las acciones funcionan
- [x] Persistencia en localStorage funciona
- [x] Datos ficticios son coherentes

### Calidad visual
- [x] Coherencia visual en todas las secciones
- [x] Tipografía correcta (Geist, JetBrains Mono)
- [x] Colores consistentes con paleta
- [x] Espaciado consistente
- [x] Radiuses consistentes
- [x] Componentes reutilizables sin variaciones
- [x] Animaciones suaves sin saltos
- [x] Hover states visibles y coherentes

### Escritorio (1280px+)
- [x] Layout correcto
- [x] Sidebar visible
- [x] Contenido bien distribuido
- [x] Tablas sin scroll
- [x] Modales centrados
- [x] Sin errores visibles

### Tablet (768-1279px)
- [x] Layout correcto
- [x] Sidebar adaptable
- [x] Contenido reflow correcto
- [x] Tablas adaptadas
- [x] Modales con padding correcto
- [x] Sin errores visibles

### Móvil (<768px)
- [x] Layout correcto
- [x] Drawer off-canvas funciona
- [x] Menú hamburguesa visible
- [x] Contenido full-width
- [x] Tablas convertidas a cards
- [x] Modales full-screen
- [x] Touch-friendly
- [x] Sin errores visibles

### Verificación final
- [x] No hay errores en consola del navegador
- [x] No hay warnings críticos
- [x] HTML semántico
- [x] CSS coherente
- [x] JavaScript funciona correctamente
- [x] Datos se cargan sin retrasos visibles
- [x] Cambios persisten correctamente
- [x] Ambos temas son legibles
- [x] Especificación completamente cumplida

---

## Notas Generales

### Verificación de Tareas
- Marcar una tarea como completada SOLO después de verificarla
- Si una tarea no puede verificarse por restricciones de acceso, dejarla pendiente
- Documentar brevemente cualquier impedimento

### Reutilización de Código
- Usar componentes existentes cuando sea posible
- Reutilizar estilos y patrones
- No crear duplicidades innecesarias

### Restricciones
- No añadir funcionalidades no solicitadas en spec.md
- No usar frameworks ni librerías adicionales
- Mantener simplicidad en la implementación
- Priorizar acabado visual y funcionalidad

---

**Lista de Tareas completada:** Noviembre 2024
