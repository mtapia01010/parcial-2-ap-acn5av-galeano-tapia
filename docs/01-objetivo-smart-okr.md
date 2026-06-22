# Objetivo del Proyecto (SMART / OKR)

**Proyecto**: ObraDOS — Tu segunda mano en la gestión de obras
**Versión del documento**: 0.1.0
**Fecha**: 2026-06-17
**Responsables**: Galeano, Daniel - Tapia, Martin 

## 1. Contexto del proyecto

**ObraDOS** es una plataforma SaaS orientada a empresas constructoras que necesitan centralizar la gestión comercial, operativa y financiera de sus obras en un único sistema.

El proyecto nace ante la fragmentación habitual en el sector: presupuestos en planillas de cálculo, avances en mensajes o planillas paralelas, certificaciones en documentos Word/PDF sin trazabilidad, cobranzas desconectadas del avance real y falta de visibilidad ejecutiva sobre rentabilidad por obra.

La solución integra, en un flujo continuo:

- Presupuestación estructurada (Ítems Globales → Ítems de Trabajo)
- Actualización por coeficientes (Mano de Obra, Materiales, Construcción)
- Gestión operativa de obra (tareas, avances, validación)
- Certificaciones quincenales (obra) y mensuales (administrativo)
- Validación por Arquitecto del cliente
- Facturación, órdenes de pago, cobranza y jornales
- Gestión documental y dashboard ejecutivo

Este documento define el objetivo general del proyecto utilizando la metodología SMART y el marco OKR, como base para la planificación, ejecución y evaluación de ObraDOS.


## 2. Objetivo general del proyecto

**Desarrollar e implementar ObraDOS**, una plataforma SaaS integral de gestión de obras para empresas constructoras, que unifique presupuestos, certificaciones, avances, cobranzas y control financiero, entregando valor medible a administradores, obradores, arquitectos y directores mediante releases incrementales gestionados con metodología ágil.


## 3. Objetivo SMART

La metodología **SMART** exige que el objetivo sea **S**pecífico, **M**edible, **A**lcanzable, **R**elevante y **T**emporalmente definido.

### 3.1 Desglose SMART

Criterio y Definición:

**S — Specific (Específico)** Diseñar y construir una plataforma SaaS multi-unidad de negocio que cubra el ciclo completo: presupuesto -> confirmación -> ejecución de obra -> certificación -> facturación -> cobranza -> dashboard ejecutivo, con roles diferenciados (Administrador, Obrador, Arquitecto, Director).
**M — Measurable (Medible)** El éxito se medirá mediante: (1) módulos funcionales entregados según requerimientos definidos, (2) reducción de tiempo en confección de presupuestos y certificados, (3) trazabilidad documental de los flujos críticos, (4) disponibilidad de KPIs financieros y operativos en dashboard.
**A — Achievable (Alcanzable)** El alcance se acota a un MVP con módulos de presupuestación, gestión de obra y control financiero, con prototipo funcional. 
**R — Relevant (Relevante)** Responde a necesidades reales del sector construcción: inflación (considerando los coeficientes aplicados al rubro), certificación quincenal/mensual, validación del arquitecto, control de cobranzas y visibilidad de rentabilidad por obra.
**T — Time-bound (Temporal)** Horizonte del proyecto: 20 semanas, con entregas incrementales de documentación y producto, y prototipo listo para demostración al cierre del período.

### 3.2 Redacción SMART consolidada

**En un plazo de 20 semanas**, desarrollar el MVP de ObraDOS, plataforma SaaS que integre los módulos de presupuestos y clientes, gestión operativa y certificaciones, y gestión financiera con dashboard, con prototipo interactivo validado con usuarios clave del sector y reducción objetivo del 40%** en tiempo administrativo para presupuestación y certificación mensual.


## 4. OKRs

### 4.1 OKRs de nivel proyecto

**Objetivo 1 (O1):** Entregar un MVP que digitalice el ciclo presupuesto–obra–cobro

ID, Key y Result

KR 1.1: Módulo de presupuestos con ítems globales, ítems de trabajo y coeficientes. Flujos de presupuesto operativos.
KR 1.2: Módulo operativo con avances, certificación quincenal y validación de arquitecto. Flujo operativo completo.
KR 1.3: Módulo financiero con órdenes de pago, cobranza y dashboard ejecutivo. KPIs visibles y actualizados.
KR 1.4: Prototipo presentable a cliente constructor. Release demostrable con vistas Admin, Obrador y Arquitecto.

**Objetivo 2 (O2):** Gestionar el proyecto con entregas ordenadas y control de cambios

ID, Key y Result

KR 2.1: Cumplir el cronograma general del proyecto. Entregas en fecha planificada.
KR 2.2: Mantener documentación y producto versionados. Avance trazable en repositorio.
KR 2.3: Gestionar desvíos de alcance con replanificación documentada. Cambios registrados y comunicados.

**Objetivo 3 (O3):** Validar el valor de ObraDOS para el mercado constructor

ID, Key y Result

KR 3.1: Cubrir el flujo de negocio integral de la constructora. Procesos críticos mapeados en el sistema.
KR 3.2: Alinear el producto con necesidades de actores clave. Requerimientos vinculados a stakeholders.
KR 3.3: Demostrar retorno operativo para el cliente piloto. Reducción medible de tiempos administrativos.



## 5. Alineación SMART <-> OKR

Elemento SMART y OKR relacionado 

Específico: plataforma SaaS integral. O1 — MVP ciclo presupuesto–obra–cobro.
Medible: módulos y KPIs. KR 1.1–1.4
Alcanzable: MVP y equipo de 2. O2 — Gestión y trazabilidad.
Relevante: sector construcción. O3 — Valor de negocio.
Temporal: 20 semanas. O2 — KR 2.1.


## 6. Indicadores de éxito del proyecto

Indicador, Línea base y Meta ObraDOS

Tiempo confección presupuesto. 4–8 horas (planillas). ≤2 horas (−50%)
Tiempo certificación mensual. 2–3 días (manual). ≤4 horas (−80%)
Trazabilidad documental. Fragmentada. Centralizada en la plataforma.
Visibilidad rentabilidad por obra. Estimación manual. Tiempo real en dashboard.


## 7. Alcance y exclusiones

**Dentro del alcance (MVP)**

- Gestión multi-unidad de negocio, clientes, presupuestos y obras
- Coeficientes de actualización (MO, Materiales, Construcción)
- Certificados de obra y administrativo
- Flujo de validación del arquitecto
- Órdenes de pago, cobranza y jornales
- Gestión documental básica
- Dashboard ejecutivo con KPIs
- Prototipo web (Administrador, Obrador, Arquitecto)

**Fuera del alcance (v1.0)**

- Integración con ERPs externos
- Facturación electrónica fiscal
- App móvil nativa
- Multi-idioma
- Firma digital certificada
- Inteligencia artificial / predicción de costos


## 8. Supuestos y restricciones

Tipo y Descripción
**Supuesto**: El cliente piloto acepta un SaaS web sin integración ERP en la primera versión.
**Supuesto**: Los coeficientes son provistos o configurados por el administrador.
**Supuesto**: Equipo de 2 integrantes con dedicación parcial al proyecto.
**Restricción**: Plazo de entrega: 20 semanas.
**Restricción**: MVP demostrable (no despliegue productivo completo).
**Restricción**: Control de versiones en repositorio del proyecto.



## 9. Criterios de cierre del objetivo general

- [ ] Módulos del MVP entregados según requerimientos definidos
- [ ] Prototipo funcional con datos representativos del negocio
- [ ] OKRs O1, O2 y O3 con mayoría de Key Results alcanzados
- [ ] Validación del Product Owner y aprobación de demo de cierre

---

## 10. Control de versión 

v0.1.0 - 2026-06-17 - Creación del documento. Objetivo general, SMART y OKRs.
