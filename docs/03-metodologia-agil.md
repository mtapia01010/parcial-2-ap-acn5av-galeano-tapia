ObraDOS — Metodología ágil de gestión del proyecto

Proyecto: ObraDOS — Tu segunda mano en la gestión de obras  
Versión: v0.3.0 · Fecha: 2026-06-19  
Autores: Martín Tapia · Daniel Galeano

1. Introducción

ObraDOS es una plataforma SaaS con varios módulos interrelacionados (comercial, operativo, financiero) y distintos perfiles de usuario: administrador, obrero, arquitecto y director. Ese contexto exige entregas parciales, validación frecuente y margen para corregir el rumbo sin detener el proyecto.

El equipo está conformado por dos integrantes con roles combinados. Por eso se adoptó un enfoque ágil que combine estructura de corto plazo con visibilidad del trabajo en curso. Este documento describe ese marco: qué metodología se eligió, por qué, y cómo se organiza el día a día del proyecto.

2. Enfoque adoptado: Scrumban

Se trabaja con un híbrido entre Scrum y Kanban, habitualmente llamado Scrumban. Scrum aporta el ritmo en ciclos de dos semanas; Kanban aporta un tablero donde se ve el estado de cada historia de usuario.

2.1. Scrum como marco principal

Los sprints duran dos semanas, alineados con la lógica quincenal del sector construcción (certificaciones y cierres de obra). Cada sprint cierra con un incremento demostrable — documentación o prototipo — y una revisión con quienes validan el producto.

Scrum encaja porque:

- el MVP se construye por módulos;
- el equipo es chico y necesita feedback rápido;
- los stakeholders clave (administrador, arquitecto) pueden opinar en cada Sprint Review sin esperar al final del proyecto.

2.2. Kanban como complemento

Paralelamente se usa un tablero Kanban con columnas: Backlog → Ready → In Progress → Review → Done. Así se ve de un vistazo qué está pendiente, qué está en curso y qué ya cumplió la definición de terminado. Se fija un límite de dos ítems en progreso a la vez, para no dispersar el esfuerzo del equipo.

En la práctica, Scrum define cuándo se planifica y se entrega; Kanban define cómo fluye cada ítem hasta Done.

3. Justificación de la elección

Los requerimientos de ObraDOS no están cerrados desde el día uno: coeficientes de actualización, certificaciones duales (obra y administrativo), validación del arquitecto y flujo financiero son dominios que conviene ir descubriendo con prototipos y demos. Un enfoque ágil permite repriorizar el backlog sin paralizar el desarrollo.

La entrega por módulos — presupuestos, obra, finanzas — se presta a incrementos integrables al cierre de cada sprint. Las Sprint Review dan espacio para validar con usuarios clave antes de invertir en el siguiente bloque. Y el plazo acotado del trabajo práctico se controla mejor con ciclos cortos que con un plan rígido de largo aliento.

3.1. Por qué no cascada

Un modelo predictivo exigiría congelar todos los requerimientos antes de escribir código. En este dominio, eso aumentaría el riesgo de diseñar módulos que no coinciden con la operación real del cliente. Preferimos validar por iteraciones y corregir a tiempo.

4. Equipo y roles

Son dos personas cubriendo las funciones esenciales de gestión, producto, desarrollo y calidad.

Martín Tapia concentra la gestión del proyecto (cronograma, riesgos), la definición técnica, la implementación del prototipo y el control de versiones en Git. En la práctica cumple como Project Manager, Tech Lead y desarrollador.

Daniel Galeano prioriza el backlog, facilita las ceremonias, mantiene el tablero Kanban y valida que cada entrega cumpla los criterios de aceptación antes de darla por cerrada. Actúa como Product Owner, Scrum Master y referente de QA.

La superposición de roles es deliberada: en un equipo de dos no tiene sentido duplicar ceremonias ni burocracia; sí tiene sentido que ambos conozcan el producto y el proceso.

5. Ceremonias

Las reuniones se mantienen livianas pero regulares:

- Sprint Planning (inicio de sprint, ~1 h 30): se elige el trabajo del backlog y se acuerda el objetivo del sprint.
- Daily Scrum (tres veces por semana, ~10 min): sincronización breve de avances y bloqueos.
- Refinamiento de backlog (mitad de sprint, ~45 min): se detallan las próximas historias de usuario.
- Sprint Review (fin de sprint, ~45 min): demo del incremento y feedback de stakeholders.
- Retrospectiva (fin de sprint, ~30 min): qué mejorar en el proceso de trabajo.

6. Artefactos

- Product Backlog: lista priorizada de historias de usuario; la mantiene el Product Owner.
- Sprint Backlog: ítems comprometidos en el sprint en curso.
- Incremento: documentación o código usable, integrado al repositorio.
- Tablero Kanban: estado visual de cada ítem.
- Definición de Done (DoD): criterios para dar un ítem por terminado.

7. Prácticas de trabajo

7.1. Definición de Done

Un ítem se considera terminado cuando:

- cumple sus criterios de aceptación;
- está integrado al repositorio;
- el tablero está actualizado;
- fue revisado en la Sprint Review;
- no quedan defectos críticos abiertos.

7.2. Cambios de alcance

Si surge un cambio relevante, el PO lo registra y estima impacto. Si afecta el plan, se replanifica en conjunto, se documenta la decisión y se comunica en la siguiente review. No se posterga el cambio ni se acumula deuda de alcance sin registrarlo.

7.3. Flujo del tablero

Los ítems avanzan en este orden:

1. Backlog — identificados pero no refinados.
2. Ready — listos para tomar en sprint.
3. In Progress — en desarrollo o documentación.
4. Review — en validación por PO o QA.
5. Done — DoD cumplida.

8. Herramientas

- Documentación del proyecto en Markdown (carpeta docs/).
- Código y snapshots del prototipo versionados con Git/GitHub.
- Seguimiento visual del backlog con tablero Kanban (PlantUML en el repo; herramienta externa opcional para la demo).

9. Conclusiones

ObraDOS se gestiona con Scrumban adaptado a un equipo reducido: sprints quincenales para ritmo y validación, tablero Kanban para transparencia. Esa combinación equilibra planificación y flexibilidad, algo necesario en un producto donde lo operativo del cliente puede desafiar supuestos del diseño inicial.

10. Control de versión

v0.3.0 (2026-06-17) — Primera redacción: metodología Scrumban, roles, ceremonias, artefactos y prácticas de trabajo.
