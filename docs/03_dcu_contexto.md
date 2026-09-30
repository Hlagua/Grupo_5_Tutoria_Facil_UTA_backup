# 03. Diseño Centrado en el Usuario (DCU - ISO 9241-210)

**Sistema:** Tutoría Fácil UTA  
**Autora responsable:** Alison Marcela Cobos Taco (@Itsuna18 - Desarrollador Back-End / Analista DCU)  

---

## 1. Contexto de Uso

* **Usuarios:** Estudiantes universitarios de pregrado de la Facultad de Ingeniería en Sistemas, Electrónica e Industrial (FISEI - UTA), cursando diversas asignaturas técnicas.
* **Tareas a realizar:** Consultar docentes asignados, revisar disponibilidad horaria en tiempo real, agendar una tutoría presencial o virtual, recibir confirmación formal y reprogramar citas ante imprevistos académicos.
* **Entorno:** Dispositivos móviles en movimiento (transporte público / bus), con iluminación ambiental variable, ruido y distracciones frecuentes (**E1**).
* **Restricciones:** Conexión de datos móviles inestable o intermitente (**E8**), pantallas táctiles reducidas y ventanas horarias limitadas de los docentes (**E6**).

---

## 2. Persona Ficticia y Escenario de Uso

### Persona: Laura Paredes
* **Edad:** 20 años.
* **Ocupación:** Estudiante de 5to Semestre de Ingeniería de Software (FISEI - UTA).
* **Comportamiento:** Realiza trayectos diarios de 45 minutos en autobús intercantonal desde Pelileo hasta el Campus Huachi en Ambato (**E1**). Utiliza un teléfono móvil de gama media y acostumbra gestionar sus tareas académicas en lapsos cortos entre clases o en el viaje.
* **Frustraciones:**
  - El tiempo muerto que transcurre mientras el docente responde un mensaje de WhatsApp (a menudo horas o al día siguiente).
  - La incomodidad de recibir confirmaciones informales ("Listo", "OK") que luego quedan sepultadas en chats personales (**E5**).
  - Perder turnos debido a que otro compañero acordó el mismo horario con el docente minutos antes (**E3**).
* **Necesidad:** Un sistema directo y confiable que le permita reservar una tutoría en menos de un minuto desde el bus y contar con un comprobante seguro.

### Escenario del Problema Actual (AS-IS)
Laura necesita una tutoría con el docente de IHC para aclarar dudas sobre las leyes de la Gestalt antes de su prueba práctica. Mientras viaja en el bus hacia la universidad, abre WhatsApp y le envía un mensaje al docente a las 18:30 p.m. El docente, que ya no está en su jornada laboral (**E6**), responde al día siguiente a las 08:15 a.m. sugiriendo dos opciones. Laura responde en su descanso de las 10:00 a.m. eligiendo el jueves a las 11:00 a.m., pero el docente le informa que ese turno ya fue asignado a otro estudiante que escribió antes (**E3**). Tras 14 minutos efectivos de atención dividida y 9 mensajes cruzados (**E4**), Laura debe volver a buscar opciones, sintiendo frustración y perdiendo tiempo valioso de estudio.

---

## 3. Journey Map del Proceso Actual (5 Etapas)

| Etapa | Acción del Estudiante | Pensamiento | Emoción | Problema / Punto de Dolor | Oportunidad en la Solución |
|:---:|---|---|---|---|---|
| **1. Buscar** | Busca el número del docente en chats grupales o sílabo. | *«¿Dónde estará el número del docente de IHC?»* | Incertidumbre | Información fragmentada y no estandarizada. | Directorio centralizado accesible en 1 clic. |
| **2. Contactar** | Redacta mensaje formal y espera respuesta por WhatsApp. | *«Ojalá me responda pronto y no se moleste por la hora.»* | Ansiedad (**E6**) | Respuestas asíncronas fuera del horario docente. | Consulta de disponibilidad autónoma 24/7 sin intermediación. |
| **3. Acordar** | Negocia horarios mediante 9 mensajes alternados. | *«Ese horario choca con mi laboratorio, ¿tendrá otro?»* | Frustración (**E4**) | Colisión con otros estudiantes y demora de 14 minutos (**E3**). | Cuadrícula de franjas horarias con actualización en tiempo real. |
| **4. Confirmar** | El docente responde un "OK" informal. | *«¿Habrá anotado bien mi nombre y la fecha?»* | Inseguridad (**E5**) | Confirmaciones ambiguas y olvidos por saturación de chats. | Generación de comprobante con código único y notificación formal. |
| **5. Cambiar** | Solicita cambio de horario por cruce imprevisto de materias. | *«Qué vergüenza pedir cambio de nuevo, va a pensar que soy irresponsable.»* | Temor / Bloqueo (**E10**) | La secretaria tiene registros en Excel desactualizados (**E7**). | Botón visible de reprogramación directa en 2 toques. |

---

## 4. Requisitos de Usuario Formalizados

1. **REQ-01 (Búsqueda y Acceso):**
   * *La persona estudiante debe poder* buscar a su docente por nombre o asignatura, *bajo* un campo de búsqueda intuitivo en pantalla principal, *para* acceder a los horarios disponibles en menos de 10 segundos (**E1, E4**).
2. **REQ-02 (Diferenciación de Disponibilidad):**
   * *La persona usuaria debe poder* visualizar con distinción gráfica y textual los horarios disponibles, ocupados y seleccionados, *bajo* cualquier condición de iluminación y con soporte de accesibilidad, *para* evitar colisiones de reserva (**E2, E3, E9**).
3. **REQ-03 (Prevención de Errores y Verificación):**
   * *La persona debe poder* examinar una pantalla de resumen con todos los datos de su cita previa a la confirmación final, *bajo* una vista estructurada y reversible, *para* validar los datos o retroceder a modificar la selección (**E10**).
4. **REQ-04 (Confirmación Confiable):**
   * *La persona estudiante debe poder* obtener una confirmación unívoca con identificador de reserva y detalles de modalidad, *bajo* retroalimentación visual clara, *para* tener certeza del agendamiento sin depender de mensajes informales (**E5, E9**).
5. **REQ-05 (Reprogramación Ágil):**
   * *La persona debe poder* solicitar el cambio de fecha u hora de una tutoría confirmada, *bajo* una acción directa desde el comprobante de cita, *para* reprogramar su horario sin cancelar ni reiniciar todo el proceso (**E1, E7, E10**).
