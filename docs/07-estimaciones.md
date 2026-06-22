ObraDOS — Estimaciones de requerimientos

Proyecto: ObraDOS — Tu segunda mano en la gestión de obras  
Consigna: Punto 7 — Estimaciones de requerimientos e historias de usuario  
Versión: v0.7.0 · Fecha: 2026-06-17  
Autores: Daniel Galeano (PO) · Martín Tapia (PM)

1. Introducción

Este documento registra las estimaciones del Product Backlog de ObraDOS. Se aplican a las doce historias de usuario definidas en el documento de requerimientos (v0.4.0) y agrupadas por milestone en el documento de milestones (v0.6.0).

Las cifras quedan reflejadas en el tablero Kanban (07-tablero-kanban.puml), como evolución del tablero del punto 6 (06-tablero-kanban.puml).

2. Técnica de estimación

Se utilizan Story Points (puntos de historia) con escala Fibonacci: 1, 2, 3, 5, 8, 13. No miden horas exactas, sino esfuerzo relativo: complejidad del dominio, incertidumbre e integración con otras historias.

Al estimar se tuvo en cuenta:

- reglas de negocio del sector construcción (coeficientes, certificaciones, validación del arquitecto);
- cantidad de criterios de aceptación por historia;
- dependencias con otras partes del flujo;
- incertidumbre técnica (por ejemplo el dashboard con varios KPIs y niveles de vista).

Las historias se compararon entre sí dentro de cada milestone para mantener coherencia.

3. Estimaciones por milestone

3.1. Milestone 1 — Administración comercial y presupuestos

- HU-001 — Registro de clientes y unidades de negocio: 5 SP. CRUD con relaciones; complejidad media.
- HU-002 — Creación de presupuestos estructurados: 8 SP. Ítems globales e ítems de trabajo, totales automáticos.
- HU-003 — Duplicación de presupuestos: 3 SP. Flujo acotado sobre una estructura ya existente.
- HU-004 — Coeficientes y confirmación de presupuesto: 8 SP. Estados, historial de ajustes y certificados base.

Subtotal M1: 24 SP.

3.2. Milestone 2 — Gestión operativa de obra

- HU-005 — Asignación de tareas a obradores: 5 SP. Planificación vinculada al presupuesto confirmado.
- HU-006 — Registro de avances por obrero: 8 SP. Interfaz responsive, evidencia fotográfica, varios registros.
- HU-007 — Validación y certificación quincenal: 8 SP. Avance ponderado y consolidación quincenal.
- HU-008 — Validación de certificado administrativo: 8 SP. Flujo del arquitecto y versionado del certificado.

Subtotal M2: 29 SP.

3.3. Milestone 3 — Gestión financiera y dashboard

- HU-009 — Generación de órdenes de pago: 8 SP. Depende de la aprobación previa del arquitecto.
- HU-010 — Registro de cobranzas: 5 SP. Medios de pago y estados configurables.
- HU-011 — Gestión de jornales a obradores: 5 SP. Obligaciones quincenales y pagos parciales.
- HU-012 — Dashboard ejecutivo con KPIs: 13 SP. Tres niveles de vista y al menos diez indicadores.

Subtotal M3: 31 SP.

4. Resumen del backlog estimado

- M1 (HU-001 a HU-004): 24 SP
- M2 (HU-005 a HU-008): 29 SP
- M3 (HU-009 a HU-012): 31 SP
- Total del MVP: 12 historias de usuario, 84 Story Points

Con un equipo de dos integrantes y sprints de dos semanas, 84 SP orientan la planificación a un horizonte de unos diez sprints, coherente con el cronograma del proyecto.

5. Tablero Kanban — evidencia en el sistema

Archivo: 07-tablero-kanban.puml (versión v0.7.0).

En el Product Backlog del tablero, cada historia muestra su estimación en Story Points. El tablero anterior (06-tablero-kanban.puml) no incluía estimaciones; este documento y el .puml del punto 7 las incorporan.

Visualización: abrir 07-tablero-kanban.puml en PlantUML Online o con la extensión PlantUML de VS Code / Cursor.

6. Control de versión

v0.7.0 (2026-06-17) — Estimaciones en Story Points para las 12 HU. Tablero actualizado en 07-tablero-kanban.puml.
