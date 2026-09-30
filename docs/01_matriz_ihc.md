# 01. Matriz de Interacción Humano-Computador (IHC)

**Sistema:** Tutoría Fácil UTA  
**Asignatura:** Interacción Humano-Computador  
**Universidad:** Universidad Técnica de Ambato (FISEI - Software)  
**Autor responsable:** Henry Daniel Lagua Flores (@Hlagua)  

---

## 1. Matriz Humano - Sistema

| Elemento | Pregunta Orientadora | Análisis y Definición del Sistema | Evidencias Relacionadas |
|---|---|---|---|
| **Personas** | ¿Quién interactúa directa o indirectamente y qué objetivo tiene? | **Usuario Primario:** Estudiantes universitarios (Laura, Carlos) que requieren agendar, confirmar y reprogramar tutorías académicas con rapidez desde su dispositivo móvil sin intermediarios manuales.<br/>**Usuarios Secundarios:** Docentes (reciben citas estructuradas sin atender mensajes de WhatsApp fuera de horario) y Secretaría (visibilidad automática de cupos y agendas). | **E1, E2, E6, E7** |
| **Sistema** | ¿Qué procesa, almacena o comunica la solución? | El sistema gestiona la disponibilidad horaria docente en tiempo real, procesa la reserva atómica de cupos evitando solapamientos o reservas duplicadas, genera códigos únicos de confirmación y permite la reprogramación inmediata. | **E3, E6, E7** |
| **Entrada y Salida** | ¿Qué acciones entrega la persona y qué respuesta devuelve el sistema? | **Entradas:** Criterios de búsqueda (materia/docente), selección de fecha y franja horaria táctil, confirmación de cita y parámetros de reprogramación.<br/>**Salidas:** Listado de docentes con disponibilidad, calendario interactivo diferenciado (disponible/ocupado), tarjeta de resumen, mensaje de confirmación inequívoco y alertas de estado de red. | **E1, E3, E8, E10** |
| **Disciplinas de Apoyo** | ¿Cómo aportan la informática, psicología cognitiva, ergonomía y diseño? | **Informática:** Sincronización concurrente de bases de datos, APIs REST y arquitectura web responsiva.<br/>**Psicología Cognitiva:** Minimización de la carga en la memoria de trabajo eliminando la necesidad de recordar 9 mensajes dispersos.<br/>**Ergonomía:** Zonas táctiles accesibles con el pulgar (>48x48 px) adaptadas para usuarios en movimiento en bus.<br/>**Diseño / IHC:** Mapeo natural de calendarios, consistencia visual y affordances evidentes en cada control interactivo. | **E1, E4, E5, E9** |
| **Estilos de Interacción** | ¿Qué estilos se usarán y por qué? | **Formularios guiados por pasos (stepper):** Reducen la complejidad del proceso dividiéndolo en selección, revisión y comprobante.<br/>**Manipulación directa:** Selección táctil de bloques horarios con retroalimentación visual inmediata (cambio de color, borde y texto de estado). | **E9, E10** |
