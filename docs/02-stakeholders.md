# ObraDOS — Análisis de Interesados (Stakeholders)

**Proyecto**: ObraDOS — Tu segunda mano en la gestión de obras.
**Versión del documento**: v0.2.0
**Fecha**: 2026-06-18
**Responsable** Galeano, Daniel - Tapia, Martin 


## 1. Introducción

El presente documento identifica y analiza a los stakeholders del proyecto ObraDOS: personas u organizaciones que influyen en el desarrollo del producto, se ven afectadas por su implementación o participan activamente en el flujo de negocio de la plataforma.

El análisis permite priorizar la comunicación, anticipar resistencias, alinear expectativas y traducir necesidades reales del sector construcción en requerimientos del producto.


## 2. Resumen del análisis

ObraDOS involucra actores con intereses distintos pero interdependientes:

- La empresa constructora busca control operativo y financiero de múltiples obras.
- Los obradores necesitan claridad en tareas, avances y pagos.
- El arquitecto del cliente** exige rigor técnico en certificaciones mensuales.
- El director requiere visibilidad estratégica para decidir inversiones y prioridades.
- El cliente desarrollador** condiciona la aprobación comercial y los cobros.

La mayor concentración de poder e interés recae en el Administrador de obra y el Director de la constructora. El Arquitecto posee poder moderado pero alto impacto en la validación de entregables. El Obrador tiene bajo poder de decisión sobre el proyecto, pero alta dependencia operativa del sistema.


## 3. Registro de interesados (Stakeholder Register)

ID - Interesado - Tipo - Rol en el ecosistema - Interés - Influencia - Actitud esperada

**ID: STK-01** 
Interesado: Director / Gerente general 
Tipo: Interno
Rol: Sponsor y decisor estratégico. 
Interés: Alto.
Influencia: Alto. 
Actitud esperada: favorable.

**ID: STK-02** 
Interesado: Administrador de obra. 
Tipo: Interno.
Rol: Usuario principal y operador del sistema. 
Interés: Alto.
Influencia: Alto. 
Actitud esperada: favorable

**ID: STK-03** 
Interesado: Obrador / Capataz de obra. 
Tipo: Interno.
Rol: Ejecutor de tareas y registro de avances. 
Interés: Alto.
Influencia: Bajo.
Actitud esperada: neutral -> favorable.

**ID: STK-04** 
Interesado: Arquitecto del cliente. 
Tipo: Externo.
Rol: Validador técnico de certificados administrativos. 
Interés: Alto. 
Influencia: Medio.
Actitud esperada: neutral.

**ID: STK-05** 
Interesado: Cliente desarrollador
Tipo: Externo
Rol: Contratante de la obra, aprueba presupuestos y paga 
Interés: Medio
Influencia: Alto
Actitud esperada: neutral.

**ID: STK-06** 
Interesado: Responsable administrativo / FinanzaS
Tipo: Interno
Rol: Gestión de cobranzas, órdenes de pago e impuestos
Interés: Alto
Influencia: Medio 
Actitud esperada: favorable

**ID: STK-07** 
Interesado: Equipo de desarrollo (Martín Tapia · Daniel Galeano)
Tipo: Interno
Rol: Construcción y evolución de la plataforma 
Interés: Alto
Influencia: Medio 
Actitud esperada: favorable

**ID: STK-08** 
Interesado: Product Owner (Daniel Galeano) 
Tipo: Interno
Rol: Priorización del backlog y validación de entregas 
Interés: Alto
Influencia: Alto 
Actitud esperada: favorable


## 4. Matriz Poder / Interés

La matriz clasifica a los interesados según su capacidad de influir en el proyecto y su nivel de involucramiento con ObraDOS.

                       INTERÉS
                Bajo            Alto
            ┌─────────────┬─────────────────┐
      Alto  │ Mantener    │ Gestionar de    │
            │ informado   │ cerca           │
PODER       │             │                 │
            │  STK-05*    │  STK-01 Director│
            │             │  STK-02 Admin   │
            │             │  STK-08 PO      │
            ├─────────────┼─────────────────┤
      Bajo  │ Monitorear  │ Mantener        │
            │             │ informado       │
            │             │                 │
            │             │  STK-03 Obrador │
            │             │  STK-04 Arq.    │
            │             │  STK-06 Finanzas│
            │             │  STK-07 Dev     │
            └─────────────┴─────────────────┘

* STK-05 Cliente desarrollador: alto poder en aprobación comercial,
  interés variable según etapa del proyecto (presupuesto / cobro).


### 4.1 Estrategia de engagement por cuadrante

**Alto poder — Alto interés**
Director, Administrador, Product Owner: Involucrar en decisiones clave, demos de sprint, validación de prioridades

**Alto poder — Bajo interés**
Cliente desarrollador (en etapas puntuales): Comunicación ejecutiva en hitos: aprobación de presupuesto y certificados

**Bajo poder — Alto interés**
Obrador, Arquitecto, Finanzas, Equipo dev: Consultas focalizadas, capacitación, feedback en módulos que usan a diario.

**Bajo poder — Bajo interés** 
Comunicación general: sin esfuerzo adicional en MVP


## 5. Perfiles detallados de stakeholders

### 5.1 STK-02 — Administrador de obra

Atributo: **Nombre referencial** - Descripción: Roberto Méndez.
Atributo: **Cargo** - Descripción: Administrador de obra — Empresa constructora
Atributo: **Organización** - Descripción: Constructora con 2 unidades de negocio, 8 obras activas
Atributo: **Experiencia** - Descripción: 12 años en gestión de obras residenciales y comerciales
Atributo: **Uso del sistema** - Descripción: Diario (8–10 horas en temporada alta) 

#### Contexto y responsabilidades

Roberto coordina el ciclo completo de cada obra asignada: desde la confección del presupuesto hasta la cobranza al cliente. Supervisa obradores, valida avances, genera certificaciones quincenales y mensuales, y reporta al director el estado financiero de cada proyecto.

Actualmente trabaja con planillas Excel, WhatsApp para avances de obra y PDFs para certificados. Pierde tiempo consolidando información y corrigiendo errores de cálculo en avance ponderado.

#### Necesidades

- Crear y duplicar presupuestos con estructura de ítems globales y de trabajo.
- Aplicar coeficientes de actualización (mano de obra, materiales, construcción).
- Asignar tareas a obradores y validar avances con evidencia.
- Generar certificados de obra (quincenal) y administrativo (mensual).
- Emitir órdenes de pago y registrar cobranzas.
- Centralizar documentación administrativa y técnica por obra.

#### Dolores actuales (pain points)

- Doble carga: certificado al cliente y liquidación al obrero en sistemas distintos.
- Errores al recalcular avance ponderado manualmente.
- Demoras en aprobación del arquitecto por falta de trazabilidad en versiones.
- Sin visión unificada de qué obras están en riesgo financiero.

#### Expectativas sobre ObraDOS

- Reducir a la mitad el tiempo de confección de presupuestos y certificados.
- Un solo lugar para ver estado de cada obra: avance físico, avance financiero y cobros.
- Flujo claro de estados (borrador → enviado → aprobado → confirmado).
- Alertas de certificados pendientes de validación y cobranzas vencidas.

#### Influencia en el proyecto

Dimensión: Poder de decisión. Nivel: Alto
Dimensión: Interés. Nivel: Alto
Nivel: Impacto si no se satisface. Nivel: Crítico — es el usuario principal del MVP |

#### Estrategia de relacionamiento

- Entrevistas quincenales durante el diseño de módulos operativos.
- Validación de prototipo en Milestone 1 y 2.
- Inclusión en sprint reviews como representante del usuario clave.

### 5.2 STK-03 — Obrador / Capataz de obra

| Atributo | Descripción |
|----------|-------------|
Atributo: **Nombre referencial**. Descripción: Juan Peralta.
Atributo: **Organización**. Descripción: Misma constructora; asignado a 1–2 obras simultáneas.
Atributo: **Experiencia**. Descripción: 8 años en oficios de construcción; uso básico de smartphone
Atributo: **Uso del sistema**. Descripción: Diario en obra (30–60 minutos para registros)

#### Contexto y responsabilidades

Juan ejecuta tareas asignadas por el administrador: instalaciones, terminaciones, relevamientos. Debe informar avances periódicos (diario, semanal o quincenal según la obra), adjuntar fotos y documentar cantidades ejecutadas. Su liquidación quincenal depende de la validación de esos avances.

Hoy reporta por WhatsApp o papel; no siempre tiene visibilidad de qué se aprobó ni cuánto le corresponde cobrar.

#### Necesidades

- Ver tareas asignadas con fechas, prioridad y responsable.
- Registrar avance por ítem de trabajo (porcentaje, cantidades, observaciones).
- Subir evidencia fotográfica desde el celular.
- Consultar historial de pagos y montos pendientes de liberación.
- Interfaz simple, pocos pasos, legible en pantalla de teléfono.

#### Dolores actuales (pain points)

- Avances enviados que no se procesan a tiempo.
- Desconocimiento del estado de validación hasta que pregunta al administrador.
- Disputas por diferencias entre lo ejecutado y lo certificado.
- Múltiples canales de comunicación sin registro único.

#### Expectativas sobre ObraDOS

- Saber en todo momento el estado de cada tarea: pendiente, en revisión, aprobada.
- Recibir notificación cuando el administrador libera un pago.
- Cargar avances en menos de 5 minutos por ítem.
- No depender del administrador para consultar su historial quincenal.

#### Influencia en el proyecto

| Dimensión                   | Nivel |

| Poder de decisión           | Bajo |
| Interés                     | Alto |
| Impacto si no se satisface  | Alto — adopción operativa en obra; riesgo de abandono del sistema en campo |

#### Estrategia de relacionamiento

- Pruebas de usabilidad con prototipo móvil-responsive.
- Historias de usuario priorizadas en Milestone 2.
- Capacitación breve en puesta en marcha piloto.


### 5.3 STK-04 — Arquitecto del cliente

| Atributo | Descripción |
|----------|-------------|
Atributo: **Nombre referencial**. Descripción: Arq. Laura Vázquez.
Atributo: **Cargo**. Descripción: Arquitecta — Representante técnico del cliente desarrollador.
Atributo: **Organización**. Descripción: Estudio de arquitectura contratado por el dueño del proyecto.
Atributo: **Experiencia**. Descripción: 15 años; supervisión de obras de edificios multifamiliares.
Atributo: **Uso del sistema**. Descripción: Mensual (revisión de certificado administrativo).

#### Contexto y responsabilidades

Laura valida mensualmente el certificado administrativo que la constructora presenta a su cliente. Debe confirmar que el avance físico declarado coincide con lo observado en obra y que los importes reflejan el contrato vigente. Puede aprobar el certificado o solicitar revisión con observaciones técnicas.

No participa en la operación diaria ni en pagos a obradores, pero su firma implícita condiciona la facturación al cliente desarrollador.

#### Necesidades

- Acceso al certificado administrativo con avance mensual y acumulado.
- Comparar versiones cuando hay observaciones y correcciones.
- Historial de ajustes por coeficientes aplicados.
- Flujo claro: pendiente → en revisión → aprobado / con observaciones.
- Documentación técnica de la obra disponible en el mismo contexto.

#### Dolores actuales (pain points)

- Certificados en PDF sin vínculo con planos o avances fotográficos.
- Versiones enviadas por email sin numeración ni trazabilidad.
- Tiempo perdido solicitando aclaraciones al administrador por teléfono.
- Desconfianza cuando los números no coinciden con visitas de obra.

#### Expectativas sobre ObraDOS

- Portal dedicado con vista de arquitecto: solo certificados y documentación técnica.
- Aprobar o rechazar con observaciones registradas en el sistema.
- Ver impacto de sus observaciones en la nueva versión del certificado.
- Reducir idas y vueltas con la constructora a un ciclo mensual ordenado.

#### Influencia en el proyecto

| Dimensión                  | Nivel 

| Poder de decisión          | Medio (veto técnico sobre certificación)
| Interés                    | Alto en hitos mensuales
| Impacto si no se satisface | Alto — bloquea cobranza al cliente y desacredita la plataforma.

#### Estrategia de relacionamiento

- Validación del flujo de certificación en Milestone 2.
- Inclusión de criterios de aceptación de HU de validación de arquitecto.
- Demo del módulo de certificados antes del go-live piloto.


## 6. Mapa de necesidades → módulos ObraDOS

| Necesidad prioritaria | Stakeholder | Módulo ObraDOS |

Necesidad: Presupuestos y coeficientes - Stakeholder: Administrador - Módulo: Presupuestación 
Necesidad: Validación de avances y certificación quincenal - Stakeholder: Administrador - Módulo: Gestión operativa 
Necesidad: Registro de avances con fotos - Stakeholder: Obrador - Módulo: Avance de obra 
Necesidad: Consulta de pagos - Stakeholder: Obrador - Módulo: Jornales / liquidaciones 
Necesidad: Aprobación certificado mensual - Stakeholder: Arquitecto - Módulo: Certificado administrativo 
Necesidad: KPIs y rentabilidad - Stakeholder: Director - Módulo: Dashboard ejecutivo 
Necesidad: Cobranzas y órdenes de pago - Stakeholder: Administrador / Finanzas - Módulo: Gestión financiera


## 7. Riesgos asociados a stakeholders

Riesgo: Resistencia al cambio por hábito en Excel/WhatsApp
Interesado: Obrador
Probabilidad: Media
Impacto: Alto
Mitigación: UX simple, capacitación, piloto en 1 obra

Riesgo: Exigencia de funcionalidades fuera de MVP
Interesado: Arquitecto
Probabilidad: Media
Impacto: Medio
Mitigación: Alcance acordado; roadmap v2 para firma digital

Riesgo: Baja adopción 
Interesado: Administrador 
Probabilidad: Baja 
Impacto: Alto
Mitigación: Sponsor visible; KPIs en dashboard desde Milestone 3


Riesgo: Demoras en aprobación de presupuestos por el cliente 
Interesado: Cliente desarrollador  
Probabilidad: Alta
Impacto: Medio
Mitigación: Estados claros y recordatorios; fuera de control del MVP


## 8. Conclusiones

El análisis confirma que el éxito de ObraDOS depende de satisfacer primero al Administrador de obra (usuario principal), garantizar adopción en campo del Obrador (interfaz ágil) y cumplir el rigor del Arquitecto en certificaciones mensuales.

Estos tres perfiles cubren el núcleo operativo del flujo presupuesto → obra → cobro y orientan la priorización del backlog en los Milestones 1 y 2. El Director y el cliente desarrollador se gestionan como stakeholders de alto poder en hitos comerciales y de cierre financiero (Milestone 3).



## 9. Control de versión de este documento

Versión: v0.2.0 
Fecha: 2026-06-17 
Cambio: Registro de interesados, matriz poder/interés y perfiles de Administrador, Obrador y Arquitecto.
