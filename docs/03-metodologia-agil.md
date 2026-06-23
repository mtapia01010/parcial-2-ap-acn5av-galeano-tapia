# ObraDOS — Metodología Ágil de Gestión del Proyecto

Proyecto: ObraDOS — Tu segunda mano en la gestión de obras  
Versión del documento: v1.0.0 · Fecha: 2026-06-21  
Responsables: Martín Tapia · Daniel Galeano  
Nota: Versión consolidada post-simulación (9a–9c) y replanteo Operativo (9b-4). Reemplaza v0.3.0.


## 1. Introducción

Este documento describe la metodología ágil adoptada para el desarrollo de ObraDOS: marco de trabajo, roles, ceremonias, artefactos y prácticas que guiarán la ejecución del proyecto.

La elección responde a la naturaleza del producto — un SaaS con múltiples módulos y stakeholders diversos — y a un equipo de 2 integrantes que requiere entregas incrementales y capacidad de adaptación ante cambios.


## 2. Enfoque adoptado: Scrum + Kanban (híbrido)

### 2.1 Framework principal — Scrum

Scrum estructura el trabajo en sprints de 2 semanas, con entregas incrementales de valor y ceremonias de alineación. Se adopta como marco principal porque:

* El producto se construye por módulos entregables de forma incremental.
* El equipo es reducido y necesita ciclos cortos de feedback.
* Los stakeholders (administrador, arquitecto) pueden validar avances en cada sprint review.
* La duración del sprint se alinea con el cierre quincenal operativo del sector construcción.

### 2.2 Complemento — Kanban

Kanban se incorpora como práctica de visualización y flujo de trabajo. Se utiliza para:

* Tablero con estados: Backlog → Ready → In Progress → Review → Done
* Seguimiento del avance de cada historia de usuario.
* Identificación de cuellos de botella.
* Límite de trabajo en progreso (WIP): máximo 2 ítems en "In Progress" a la vez.

### 2.3 Síntesis del enfoque híbrido

* **Planificación:** Scrum (Sprint Planning quincenal) · Kanban (Flujo continuo)
* **Ejecución:** Scrum (Objetivo de sprint) · Kanban (Tablero visual)
* **Entrega:** Scrum (Incremento al cierre) · Kanban (Ítems en Done)
* **Mejora:** Scrum (Retrospectiva) · Kanban (Análisis de tiempos por columna)
* **Priorización:** Scrum (PO en backlog) · Kanban (Sistema Pull desde Ready)

*Denominación:* Scrumban (Scrum para ritmo y compromiso; Kanban para visibilidad y control de flujo).


## 3. Justificación de la elección

* **Requerimientos evolutivos:** El backlog se reprioriza sin detener el equipo ante cambios del negocio.
* **Entrega por módulos:** Presupuestos, obra y finanzas son incrementos integrables bajo el modelo de sprint.
* **Múltiples stakeholders:** La Sprint Review permite validación temprana con usuarios clave.
* **Plazo acotado:** Sprints de 2 semanas permiten controlar el avance y replanificar.
* **Trazabilidad:** Cada entrega queda vinculada a documentación y repositorio.

### 3.1 Por qué no enfoque predictivo (cascada)

Un modelo en cascada obligaría a cerrar todos los requerimientos antes de desarrollar. En ObraDOS, la complejidad de coeficientes, certificaciones duales y validación externa del arquitecto hace preferible validar por iteraciones, reduciendo retrabajo.


## 4. Equipo y roles

* **Martín Tapia** (Project Manager · Tech Lead · Desarrollador)  
  *Responsabilidad:* Cronograma, hitos, riesgos, arquitectura, implementación y control de versiones en Git.
* **Daniel Galeano** (Product Owner · Scrum Master · QA)  
  *Responsabilidad:* Backlog, criterios de aceptación, facilitación de ceremonias, tablero Kanban y validación de entregas.


## 5. Ceremonias

**Sprint Planning** (Inicio de sprint · 1,5 h): Seleccionar trabajo del backlog y definir el objetivo del sprint.
**Daily Scrum** (3 veces por semana · 10 min): Sincronizar avance y destrabar bloqueos.
**Refinamiento de backlog** (Mitad de sprint · 45 min): Detallar próximos ítems y aclarar requerimientos.
**Sprint Review** (Fin de sprint · 45 min): Demo del incremento y feedback con stakeholders.
**Retrospectiva** (Fin de sprint · 30 min): Analizar oportunidades de mejora en el proceso.


## 6. Artefactos

**Product Backlog:** Lista priorizada de requerimientos e historias de usuario (Responsable: Daniel Galeano - PO).
**Sprint Backlog:** Ítems comprometidos en el sprint actual (Responsable: Ambos).
**Incremento:** Documentación o software terminado y usable (Responsable: Martín Tapia).
**Tablero Kanban:** Estado visual de cada ítem (Responsable: Daniel Galeano - SM).
**Definición de Done:** Criterios para dar un ítem por terminado (Responsable: Ambos - ver sección 7).


## 7. Prácticas de trabajo

### 7.1 Definición de Done (DoD)

Un ítem se considera **Done** cuando:

* Cumple con sus criterios de aceptación.
* Está integrado en el repositorio.
* El tablero fue actualizado.
* Fue revisado en la Sprint Review.
* No tiene defectos críticos abiertos.

### 7.2 Gestión de cambios de alcance

1. El PO registra el cambio y evalúa el impacto.
2. El SM facilita la replanificación si el impacto es significativo.
3. Se documenta la decisión tomada.
4. Se informa en la siguiente review.

### 7.3 Flujo del tablero Kanban

`Backlog -> Ready -> In Progress -> Review -> Done`

**Backlog:** Ítem identificado, pendiente de refinamiento.
**Ready:** Ítem listo para tomar en sprint.
**In Progress:** En desarrollo o documentación.
**Review:** En validación por PO / QA.
**Done:** Cumple con la DoD.


## 8. Herramientas

**Git / GitHub:** Control de versiones.
**Markdown (docs/):** Documentación del proyecto.
**Tablero Kanban:** Seguimiento de ítems mediante PlantUML + herramienta visual.


## 9. Adaptación metodológica durante la ejecución

Durante la simulación de desarrollo (iteraciones 9b-1 a 9b-3), el cliente indicó que el módulo Operativo basado en tareas sueltas no reflejaba su operación real. El equipo aplicó los pilares ágiles sin cambiar el marco Scrumban:

**Transparencia:** Demo temprana al administrador y referente del cliente.
**Inspección:** Feedback registrado formalmente.
**Adaptación:** Replanteo 9b-4; snapshots 9b-1…9b-3 congelados como evidencia.

**Documentos de referencia:**
`docs/10-cambio-metodologico.md` — decisión de gestión e impacto en HU.
`docs/09b-4-replanteo-operativo.md` — especificación del nuevo modelo Operativo.
`docs/final/04-requerimientos.md` — HU-005–007 redactadas según el modelo acordado.

La metodología base no se reemplazó; se replanificó el backlog del M2 y se pospuso la HU-008 a la iteración 9b-5.

## 10. Conclusiones

ObraDOS se gestiona con Scrumban, adaptado a un equipo de 2 integrantes: Scrum aporta ritmo y validación periódica; Kanban aporta transparencia en el flujo de trabajo. El replanteo del módulo Operativo demuestra la capacidad del equipo de adaptar el alcance sin abandonar el marco ágil.

## 11. Control de versión de este documento

**v0.3.0** (2026-06-17): Metodología Scrumban, roles, ceremonias, artefactos y prácticas de trabajo.
**v1.0.0** (2026-06-21): Consolidación post-simulación. Incorporación de adaptación metodológica (replanteo 9b-4).