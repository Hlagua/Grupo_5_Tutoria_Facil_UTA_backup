# 04. Principios de Diseño, Leyes Gestalt y Guía de Estilo

**Sistema:** Tutoría Fácil UTA  
**Autores responsables:** Melany Saleth Cevallos Goyes (@SalyC15) y Henry Daniel Lagua Flores (@Hlagua)  

---

## 1. Decisiones de Interacción y Factores Humanos

| Concepto de IHC | Decisión Concreta en el Prototipo | Justificación y Evidencia |
|---|---|---|
| **Metáforas del Mundo Real** | Se emplea la metáfora de **"Agenda de Citas"** y **"Tarjeta / Ticket de Reserva"**. El comprobante final adopta la estructura reconocible de un boleto o pase de abordaje, lo que transmite inmediatamente validez y certidumbre. | Aprovecha los modelos mentales preexistentes del estudiante (**E9**), eliminando la confusión generada por confirmaciones en texto libre. |
| **Affordance y Mapeo** | Los bloques horarios libres poseen esquinas redondeadas, fondo blanco con borde contrastante y sombra sutil que sugiere capacidad de ser presionados (*affordance táctil*). El mapeo espacial ordena los días en secuencia horizontal y las horas en orden cronológico vertical. | Facilita la selección inmediata e intuitiva; los horarios ocupados aparecen deshabilitados y planos para prevenir selecciones erróneas (**E3, E9**). |
| **Manipulación Directa** | El usuario toca directamente el casillero del horario que desea y observa la transformación inmediata del elemento a estado "Seleccionado" (cambio de fondo a rojo UTA suave, borde guinda y check de verificación). | Otorga control y sensación de inmediatez (**E10**), sin pantallas intermedias innecesarias. |
| **Retroalimentación del Sistema** | Notificaciones visuales de estado continuo: indicador de progreso ante conexiones lentas (*"Sincronizando con secretaría UTA..."*) y banner de confirmación en verde esmeralda con código identificador único. | Brinda certidumbre al usuario ante variabilidad de la conexión móvil (**E8**) y previene la ambigüedad (**E3, E5**). |
| **Reducción de Carga Cognitiva** | Flujo en embudo estructurado en 2 fases simples (Selección ➔ Resumen ➔ Comprobante). Se presenta únicamente la información imprescindible en cada paso, evitando sobrecarga mental. | Evita que el estudiante deba memorizar datos o contrastar calendarios manualmente (**E4, E5**). |
| **Mitigación del Riesgo Cultural** | Ninguna acción crítica o estado depende con exclusividad de un icono aislado o un color particular. Todo icono (ej. 🚫, ✓, 🔄) va invariablemente emparejado con su etiqueta de texto descriptivo. | Garantiza la accesibilidad para usuarios con baja visión y evita interpretaciones culturales erróneas de simbología abstracta (**E2, E9**). |

---

## 2. Aplicación Justificada de Tres Leyes de la Gestalt

1. **Ley de Proximidad:**
   * *Aplicación:* En la Pantalla 1 y Pantalla 2, la información relativa al docente (nombre, materia asignada, cupos disponibles y botón de acción) se encuentra encapsulada dentro de un contenedor perimetral común con espaciado interno equilibrado (*padding 15px*).
   * *Justificación perceptiva:* La mente humana agrupa visualmente los elementos próximos, asegurando que el estudiante vincule inequívocamente los horarios con el docente respectivo sin confundirlos con tarjetas adyacentes.

2. **Ley de Semejanza:**
   * *Aplicación:* Todos los horarios con estado **"Disponible"** comparten idénticas propiedades morfológicas y cromáticas: fondo blanco, borde verde tenue y tipografía negra destacada. De manera homóloga, todos los horarios **"Ocupados"** comparten fondo gris opaco y texto atenuado.
   * *Justificación perceptiva:* Permite al estudiante realizar un escaneo visual periférico instantáneo para localizar los cupos libres sin necesidad de leer detalladamente cada horario.

3. **Ley de Región Común / Figura-Fondo:**
   * *Aplicación:* La tarjeta de confirmación en la Pantalla 4 y el bloque de reprogramación están delimitados por cajas contenedoras con elevación sutil que contrastan netamente contra el fondo general neutro `#F9FAFB`.
   * *Justificación perceptiva:* Establece una clara jerarquía visual donde la información crítica de la cita emerge como "figura", captando el foco atencional del estudiante sin dispersión.

---

## 3. Mini Guía de Estilo Aplicada

### A. Tipografía Institucional
* **Familia tipográfica:** Segoe UI, Roboto, Sans-serif (máxima legibilidad en pantallas móviles).
* **Encabezado principal (H1):** 20px / 22px Bold — Color `#FFFFFF` sobre barra institucional.
* **Encabezado de sección (H2):** 15px / 16px Bold — Color `#111827`.
* **Cuerpo de texto (Body):** 12px / 13px Regular — Color `#374151`.
* **Texto auxiliar / Etiquetas (Caption):** 10px / 11px SemiBold — Mayúsculas para estados (`DISPONIBLE`, `OCUPADO`).

### B. Paleta Cromática y Contraste (Cumple WCAG AA)
* **Color Primario Institucional:** Rojo Guinda UTA (`#8B0000`) — Razón de contraste 5.8:1 con texto blanco.
* **Color Secundario / Acento:** Azul Marino (`#1E40AF`) — Destinado a acciones de gestión y reprogramación.
* **Estado Éxito:** Verde Esmeralda (`#15803D`) sobre contenedor suave (`#DCFCE7`).
* **Estado Deshabilitado / Ocupado:** Gris Neutro (`#9CA3AF`) sobre fondo (`#F3F4F6`).
* **Fondo General de Aplicación:** Neutro Claro (`#F9FAFB`).

### C. Componentes Estándar
* **Botón Primario de Acción:** Altura mínima de 48px, esquinas redondeadas (radio 8px), texto centrado en negrita (cumple norma de ergonomía táctil).
* **Tarjeta de Docente / Cita:** Contenedor blanco con borde suave (`#E5E7EB`) y elevación de 1px.
* **Slot de Horario:** Altura mínima 48px, selector táctil de fácil activación con el pulgar.
