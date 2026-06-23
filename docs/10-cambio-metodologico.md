ObraDOS — Ajuste metodológico (Consigna 5 / Fase 3)

Proyecto: ObraDOS — Tu segunda mano en la gestión de obras  
Versión: v1.1.0 · Fecha: 2026-06-21  
Sprint afectado: S6–S7 (M2 — Gestión operativa)  
Autores: Daniel Galeano (PO / SM) · Martín Tapia (PM / Dev)

1. Qué pasó

Durante la demo del módulo Operativo (HU-005, HU-006 y HU-007), el administrador de la constructora y referentes del cliente indicaron que el prototipo no refleja su forma de trabajo.

El diseño inicial planteaba tareas sueltas, precios del presupuesto comercial y certificaciones por calendario. En la práctica trabajan con la misma grilla del presupuesto (ítem global → ítem de trabajo), tarifas obrero aparte, liberación del cliente antes de asignar al obrero, y cierres de pago cuando el admin lo decide — no en fechas fijas.

Si Operativo no se parece a las planillas que ya usan, el producto sería difícil de adoptar.

2. Qué decidimos

- Mantener el prototipo anterior como evidencia de lo evaluado; no se reescribe.
- Replanteear el módulo Operativo según el modelo acordado con el cliente.
- Posponer HU-008 (certificado administrativo y validación del arquitecto) hasta cerrar el replanteo.
- Convocar backlog refinement y replanificar el alcance del M2.
- Actualizar requerimientos, prototipo, tablero Kanban y este documento.

3. Modelo acordado (resumen)

Dos capas sobre la misma estructura:

- Comercial: presupuesto confirmado, precios al cliente, coeficientes reajustables en lo no realizado.
- Operativo: certificado de obra generado al confirmar, precios obrero, mismos coeficientes con ajuste por ítem si hace falta.

Flujo de trabajo:

Presupuesto confirmado → certificado de obra → cliente/arquitecto libera ítems → admin habilita al obrero → obrero registra avance → admin valida y cierra tramo (ancla de pago) → avance de obra actualizado.

4. Cómo lo gestionamos (Scrumban)

- Transparencia: demo temprana con el stakeholder clave.
- Inspección: feedback registrado en este documento y en el replanteo operativo.
- Adaptación: HU-005, HU-006 y HU-007 se replantean en un solo entregable; HU-008 queda para después.
- Kanban: se detiene HU-008 hasta cerrar el replanteo, para no construir sobre un diseño incorrecto.

No cambiamos la metodología (Scrumban, v0.3.0); ajustamos backlog y cronograma del M2.

5. Impacto en historias de usuario

- HU-005: de tareas asignadas → certificado de obra y habilitación del obrero.
- HU-006: de avances sobre tareas → avances sobre ítems del certificado.
- HU-007: de certificación automática por calendario → validación y cierre manual del admin.
- HU-008: pospuesta (certificado administrativo y arquitecto).

6. Lecciones aprendidas

1. Validar con el cliente que la interfaz se parezca a lo que ya usan antes de proponer módulos nuevos.
2. Separar economía cliente y economía obrero, aunque compartan la misma estructura.
3. Tratar liberación (cliente) y habilitación (admin) como pasos distintos.
4. Los cierres de pago son eventos de negocio, no fechas de calendario.