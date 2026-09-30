# 02. Calidad de Uso (ISO 9241-11) y Accesibilidad (POUR)

**Sistema:** Tutoría Fácil UTA  
**Autores responsables:** Alison Cobos Taco (@Itsuna18) y Henry Lagua Flores (@Hlagua)  

---

## 1. Indicadores de Usabilidad Medibles (ISO 9241-11)

| Dimensión | Indicador y Forma de Medir | Meta Establecida | Justificación en el Caso (E1 a E10) |
|---|---|---|---|
| **Efectividad** | Porcentaje de estudiantes que completan la reserva de una tutoría de forma autónoma, sin cometer errores críticos ni colisionar con horarios ya ocupados.<br/>`Fórmula: (Reservas exitosas sin ayuda / Total de intentos) * 100` | **Meta: ≥ 95% de éxito** | En el proceso anterior se evidenció que 3 de cada 12 solicitudes intentaban seleccionar horarios ocupados y 4 derivaban en confirmaciones ambiguas (**E3**). |
| **Eficiencia** | Tiempo medio invertido para concretar una reserva (desde la selección del docente hasta la obtención del código de confirmación) y número total de toques/acciones.<br/>`Fórmula: Cronometraje en segundos y contador de toques` | **Meta: ≤ 90 segundos y ≤ 5 toques** | El proceso previo por WhatsApp demandaba un promedio de 14 minutos y el intercambio de 9 mensajes (**E4**). |
| **Satisfacción y Recuperación de Errores** | Nivel de satisfacción subjetiva mediante la escala estandarizada SUS (System Usability Scale) y tasa de recuperación autónoma ante la necesidad de modificar o reprogramar la cita.<br/>`Fórmula: Cuestionario SUS (0-100) y prueba de cambio de cita` | **Meta: SUS ≥ 85 puntos y 100% de recuperabilidad** | Corrige el olvido de citas al separarlas del chat informal (**E5**) y garantiza la capacidad de corregir o reprogramar sin frustración (**E10**). |

---

## 2. Decisiones de Accesibilidad (Principios POUR)

| Principio | Decisión Aplicada en la Solución | Mecanismo de Verificación en el Prototipo |
|---|---|---|
| **Perceptible** | Contraste de texto y elementos de interfaz con ratio superior a **4.5:1** (nivel WCAG AA). Los estados de disponibilidad de horario (**Disponible, Ocupado, Seleccionado**) cuentan siempre con texto e icono explicativo; nunca se transmite información únicamente mediante el color (**E2, E9**). | Inspección mediante el Analizador de Contraste de Color (CCA) y validación de presencia de etiquetas textuales en cada componente. |
| **Operable** | Navegación secuencial por teclado (tecla `Tab`, `Espacio` y `Enter`) con indicador de foco visual de 2px en azul `#1E40AF`. Soporte total de ampliación de pantalla al **200%** sin solapamiento de contenedores ni pérdida de funcionalidad (**E2**). | Recorrido completo del flujo utilizando únicamente el teclado físico y emulación de zoom del navegador al 200%. |
| **Comprensible** | Estructura de navegación predecible con lenguaje claro y consistente (etiquetas: Docente, Asignatura, Fecha, Modalidad). El sistema provee un resumen antes de la confirmación definitiva y opciones explícitas de cancelación/retorno (**E3, E10**). | Evaluación con usuario midiendo la comprensión de términos y la facilidad para volver a la pantalla anterior sin pérdida de datos. |
| **Robusto** | Implementación de etiquetas semánticas y atributos ARIA (`aria-label`, `aria-selected`, `aria-live` para avisos de conectividad o demoras del servidor), garantizando compatibilidad con lectores de pantalla como NVDA y TalkBack (**E2, E8**). | Auditoría de código semántico y verificación de lectura asistida mediante software lector de pantalla. |
