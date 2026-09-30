# Grupo 5 - Tutoría Fácil UTA 🎓

**Asignatura:** Interacción Humano-Computador  
**Nivel:** Quinto Semestre - FISEI  
**Carrera:** Ingeniería de Software  
**Institución:** Universidad Técnica de Ambato (UTA)  
**Semestre:** 2026

---

## 1. Problema de Diseño

La Facultad de Ingeniería en Sistemas, Electrónica e Industrial (FISEI) coordinaba sus tutorías académicas a través de canales informales (mensajes de WhatsApp, hojas de cálculo manuales y agendas personales). Este proceso provocaba tiempos muertos elevados (14 minutos y 9 mensajes promedio por solicitud), cruces de citas en horarios ya ocupados, confirmaciones ambiguas y desactualización de registros en secretaría.

**Tutoría Fácil UTA** es una solución web móvil interactiva diseñada bajo la norma **ISO 9241-210 (Diseño Centrado en el Usuario)** e **ISO 9241-11 (Usabilidad)**, que permite a los estudiantes consultar en tiempo real la disponibilidad docente, reservar su tutoría con certeza atómica en menos de 90 segundos, recibir un comprobante formal con código único y reprogramar su cita de forma autónoma y sin fricciones.

---

## 2. Integrantes del Equipo y Roles

| Integrante | Usuario GitHub | Correo Institucional | Rol Oficial | Artefacto Asignado en la Prueba |
|---|---|---|---|---|
| **Alison Marcela Cobos Taco** | [@Itsuna18](https://github.com/Itsuna18) | tacomarcelab@gmail.com | Desarrollador Back-End / Analista DCU | Análisis DCU, Contexto de uso, Persona, Journey Map y Requisitos |
| **Melany Saleth Cevallos Goyes** | [@SalyC15](https://github.com/SalyC15) | mcevallos8901@uta.edu.ec | Desarrollador Front-End | Prototipo interactivo móvil (4 pantallas) y Mini Guía de Estilo |
| **Carlos Giovanni Ramos Jácome** | [@carlitosgiovanniramos](https://github.com/carlitosgiovanniramos) | carlos.giovanni.ramos.work@gmail.com | Tester / QA Support | Protocolo de validación, prueba cruzada con usuario e iteración Antes/Después |
| **Henry Daniel Lagua Flores** | [@Hlagua](https://github.com/Hlagua) | hlagua6116@uta.edu.ec | QA (Quality Assurance) / Arquitecto IHC | Matriz humano-sistema, Indicadores ISO 9241-11, Accesibilidad POUR y Gestalt |

---

## 3. Enlaces Oficiales del Proyecto

* **Prototipo Interactivo en Figma:** [Ver Prototipo Navegable en Figma](https://www.figma.com/design/Grupo5TutoriaFacilUTA/Tutoria-Facil-UTA-Prototipo-IHC) (Permisos de vista habilitados para evaluación docente).
* **Documentación Técnica Integral (PDFs):** Disponibles en la carpeta [`docs/`](docs/).
* **Evidencia de Trabajo Grupal (PDF para Moodle):** [`Evidencia_GitHub_Grupo.pdf`](Evidencia_GitHub_Grupo.pdf).

---

## 4. Estructura del Repositorio

```text
Grupo_5_Tutoria_Facil_UTA/
├── README.md                                # Presentación del equipo, problema, enlaces y resumen
├── docs/                                    # Evidencias del análisis y diseño (PDF y Markdown)
│   ├── 01_matriz_ihc.pdf                    # Matriz humano-sistema con evidencias E1 a E10
│   ├── 01_matriz_ihc.md
│   ├── 02_usabilidad_accesibilidad.pdf      # 3 indicadores de usabilidad y 4 decisiones POUR
│   ├── 02_usabilidad_accesibilidad.md
│   ├── 03_dcu_contexto.pdf                  # Contexto, persona, escenario, journey map y 5 requisitos
│   ├── 03_dcu_contexto.md
│   ├── 04_decisiones_diseno.pdf              # Metáforas, affordance, leyes Gestalt y guía de estilo
│   └── 04_decisiones_diseno.md
├── prototipo/                               # Prototipo y capturas de pantalla
│   ├── capturas/
│   │   ├── pantalla_1_inicio_busqueda.png
│   │   ├── pantalla_2_docente_horario.png
│   │   ├── pantalla_3_resumen_confirmacion.png
│   │   ├── pantalla_4_confirmada_reprogramacion.png
│   │   ├── pantalla_4_iteracion_antes.png
│   │   └── pantalla_4_iteracion_despues.png
│   └── enlace_prototipo.md                  # Enlace navegable y recorrido paso a paso
├── evaluacion/                              # Evaluación con usuario externo e iteración
│   └── prueba_iteracion.md                  # Protocolo de prueba cruzada, hallazgo y mejora antes/después
└── Evidencia_GitHub_Grupo.pdf               # Documento compilado de trazabilidad y colaboración
```

---

## 5. Resumen de la Prueba Cruzada y Mejora Aplicada

* **Participante evaluado:** Kevin Morales (Estudiante de 5to de Software, Grupo 2 de IHC - Usuario externo).
* **Tarea solicitada:** *«Reserve una tutoría para el jueves y luego cambie el horario acordado»*.
* **Hallazgo:** En la primera versión del prototipo (v1.0), el usuario completó la reserva en 108 segundos, pero al intentar reprogramar se desorientó porque la opción era un texto pequeño subrayado (`cambiar cita (click aqui)`) sin contenedor ni affordance táctil claro, creyendo que debía abandonar el sistema y reiniciar desde cero.
* **Mejora Aplicada (Iteración v1.1):** Se rediseñó la sección de reprogramación en la Pantalla 4 incorporando una tarjeta destacada en azul suave (`#EFF6FF`) con un **botón primario de reprogramación** en azul marino (`#1E40AF`), con icono `🔄` y texto explícito: *«Reprogramar / Cambiar Horario»*.
* **Impacto Medido:** El tiempo de reprogramación disminuyó de **108 segundos a 42 segundos** y la satisfacción SUS escaló de **72 a 94 puntos**, garantizando la recuperabilidad exigida en la evidencia **E10**.

---

## 6. Trazabilidad de Colaboración en GitHub

| Integrante | Issue Asignado | Rama Feature | Commits Clave | Pull Request (PR) | Revisor Cruzado |
|---|:---:|:---:|:---:|:---:|:---:|
| **Alison Cobos** | [#1 (Cerrado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/issues/1) | `feature/alison-dcu-requisitos` | `feat(dcu): ...`<br/>`feat(journey): ...` | [#5 (Mergeado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/pull/5) | Henry Lagua (@Hlagua) |
| **Melany Cevallos** | [#2 (Cerrado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/issues/2) | `feature/melany-ui-prototipo` | `feat(ui): ...`<br/>`feat(styleguide): ...` | [#7 (Mergeado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/pull/7) | Carlos Ramos (@carlitosgiovanniramos) |
| **Carlos Ramos** | [#3 (Cerrado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/issues/3) | `feature/carlos-evaluacion-iteracion` | `test(qa): ...`<br/>`test(iteracion): ...` | [#8 (Mergeado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/pull/8) | Melany Cevallos (@SalyC15) |
| **Henry Lagua** | [#4 (Cerrado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/issues/4) | `feature/henry-ihc-accesibilidad` | `feat(ihc): ...`<br/>`fix(core): ...` | [#6 (Mergeado)](https://github.com/Hlagua/Grupo_5_Tutoria_Facil_UTA/pull/6) | Alison Cobos (@Itsuna18) |
