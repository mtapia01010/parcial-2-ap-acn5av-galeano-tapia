ObraDOS — Análisis de requerimientos e historias de usuario

Proyecto: ObraDOS — Tu segunda mano en la gestión de obras  
Versión: v0.4.0 · Fecha: 2026-06-17  
Autores: Daniel Galeano (PO) · Martín Tapia (PM)

1. Introducción

Este documento reúne el análisis de requerimientos del MVP de ObraDOS y las doce historias de usuario que componen el Product Backlog inicial. El análisis parte del flujo de negocio típico de una constructora (presupuesto, obra, certificación, cobro), de los perfiles definidos en el documento de stakeholders y de los objetivos del proyecto (SMART/OKR).

Las historias de usuario están redactadas con criterios de aceptación verificables. Cada una se identifica con el código HU-001 a HU-012; ese mismo código se utilizará en el tablero Kanban como ítem de trabajo.

2. Alcance del análisis

2.1. Dentro del alcance (MVP)

- Organización: empresa, unidades de negocio, clientes.
- Comercial: presupuestos, coeficientes, estados y confirmación.
- Operativo: obras, tareas, avances, certificación quincenal.
- Contractual: certificado administrativo y validación del arquitecto.
- Financiero: órdenes de pago, cobranza, jornales.
- Analítica: dashboard ejecutivo (empresa, unidad de negocio, obra).
- Documental: repositorio básico por presupuesto u obra.

2.2. Fuera del alcance (MVP)

Integración ERP, facturación electrónica fiscal, aplicación móvil nativa, firma digital certificada, multi-idioma e inteligencia artificial predictiva.

3. Requerimientos funcionales

3.1. Organización

- RF-001 (Alta · HU-001): Registrar unidades de negocio bajo la empresa constructora.
- RF-002 (Alta · HU-001): Registrar clientes asociados a una unidad de negocio.

3.2. Comercial

- RF-003 (Alta · HU-002): Crear presupuestos con ítems globales e ítems de trabajo (descripción, unidad, cantidad, precio, peso de avance, tipo de coeficiente).
- RF-004 (Alta · HU-002): Calcular automáticamente totales por ítem global y por presupuesto.
- RF-005 (Media · HU-003): Duplicar un presupuesto existente con su estructura.
- RF-006 (Alta · HU-004): Gestionar estados del presupuesto: Borrador, Enviado, En Revisión, Aprobado, Rechazado, Confirmado.
- RF-007 (Alta · HU-004): Aplicar coeficientes de Mano de Obra, Materiales y Construcción por ítem, con historial de ajustes.

3.3. Operativo

- RF-008 (Alta · HU-004): Al confirmar un presupuesto, generar certificado de obra y certificado administrativo.
- RF-009 (Alta · HU-005): Asignar tareas a obradores con fecha, prioridad y responsable.
- RF-010 (Alta · HU-006): Permitir al obrero registrar avance por ítem (porcentaje, cantidades, observaciones, fotos).
- RF-011 (Alta · HU-007): Validar o rechazar avances informados por el administrador.
- RF-012 (Alta · HU-007): Calcular avance ponderado de ítem, ítem global y obra.
- RF-013 (Alta · HU-007): Generar certificación quincenal consolidada para obradores.

3.4. Contractual

- RF-014 (Alta · HU-008): Generar certificado administrativo mensual alimentado por avances quincenales.
- RF-015 (Alta · HU-008): Permitir al arquitecto aprobar o solicitar revisión del certificado con observaciones.

3.5. Financiero y analítica

- RF-016 (Alta · HU-009): Generar órdenes de pago desde certificados aprobados (cliente, obra, importes, IVA, vencimiento).
- RF-017 (Alta · HU-010): Registrar cobranzas con medios de pago configurables y estados Pendiente, Parcial, Cobrado, Vencido.
- RF-018 (Alta · HU-011): Gestionar obligaciones y pagos quincenales de jornales a obradores.
- RF-019 (Alta · HU-012): Mostrar dashboard con KPIs a nivel empresa, unidad de negocio y obra.

3.6. Documental

- RF-020 (Media · HU-002, HU-006): Centralizar documentación administrativa y técnica por obra, con permisos por rol.

4. Requerimientos no funcionales

- RNF-001 (Usabilidad): Interfaz usable en escritorio para el administrador y responsive para el obrero. Criterio: prototipo validado en al menos tres roles sin asistencia.
- RNF-002 (Rendimiento): Cálculo de avance ponderado y totales de presupuesto en menos de 2 segundos. Criterio: prueba con presupuesto de al menos 50 ítems de trabajo.
- RNF-003 (Seguridad): Acceso diferenciado por rol (Administrador, Obrador, Arquitecto, Director). Criterio: cada rol ve solo los módulos autorizados.
- RNF-004 (Trazabilidad): Historial de versiones en presupuestos, certificados y coeficientes. Criterio: cada cambio registra fecha y usuario.
- RNF-005 (Disponibilidad): Plataforma web accesible el 99 % en horario laboral en piloto.
- RNF-006 (Escalabilidad): Soporte para varias unidades de negocio y obras simultáneas. Criterio: prueba con al menos 3 unidades y 10 obras simuladas.
- RNF-007 (Mantenibilidad): Código y documentación versionados en Git. Criterio: cada incremento con commit identificable.
- RNF-008 (Portabilidad): Prototipo funcional en Chrome, Edge y Firefox actuales.

5. Reglas de negocio

- RN-001: Cada obra se asocia a un único presupuesto previamente confirmado.
- RN-002: Un cliente puede tener múltiples presupuestos y múltiples obras.
- RN-003: El total de un ítem global es la suma de sus ítems de trabajo.
- RN-004: El total del presupuesto es la suma de todos los ítems globales.
- RN-005: Cada ítem de trabajo tiene un tipo de coeficiente: Mano de Obra, Materiales o Construcción.
- RN-006: La certificación quincenal consolida avances del período y habilita la liquidación al obrero.
- RN-007: El certificado administrativo es mensual y alimenta la facturación al cliente.
- RN-008: Sin aprobación del arquitecto no se genera orden de pago al cliente.
- RN-009: El avance de obra se calcula ponderando el peso relativo de cada ítem de trabajo.
- RN-010: Los medios de pago pueden incluir o excluir ciertos impuestos según configuración.

6. Trazabilidad con el flujo de negocio

El flujo end-to-end del negocio queda cubierto por los requerimientos e historias siguientes:

1. Estructura organizacional → RF-001, RF-002 · HU-001
2. Creación de presupuesto → RF-003, RF-004 · HU-002
3. Duplicación de presupuestos → RF-005 · HU-003
4. Envío y aprobación comercial → RF-006 · HU-004
5. Actualización por coeficientes → RF-007 · HU-004
6. Confirmación y certificados base → RF-008 · HU-004
7. Asignación de tareas → RF-009 · HU-005
8. Avance de obra → RF-010 · HU-006
9. Validación y avance ponderado → RF-011, RF-012 · HU-007
10. Certificación quincenal → RF-013 · HU-007
11. Certificado administrativo → RF-014 · HU-008
12. Validación del arquitecto → RF-015 · HU-008
13. Órdenes de pago → RF-016 · HU-009
14. Cobranza → RF-017 · HU-010
15. Jornales → RF-018 · HU-011
16. Dashboard → RF-019 · HU-012

Las dieciséis etapas del flujo tienen requerimiento e historia de usuario asociados (cobertura completa).

7. Historias de usuario

Convenciones: prioridad Alta, Media o Baja; stakeholder principal según el registro de interesados (STK-01 Director, STK-02 Administrador, STK-03 Obrador, STK-04 Arquitecto, STK-06 Finanzas).

7.1. HU-001 — Registro de clientes y unidades de negocio

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero registrar unidades de negocio y clientes con sus datos comerciales, para organizar la cartera comercial y asociar presupuestos y obras correctamente.

Criterios de aceptación:

- CA-1: Puedo crear, editar y listar unidades de negocio.
- CA-2: Puedo registrar clientes con nombre, contacto y unidad de negocio asociada.
- CA-3: Un cliente puede tener múltiples presupuestos y obras vinculados.
- CA-4: La búsqueda de clientes filtra por nombre o unidad de negocio.
- CA-5: Solo usuarios con rol Administrador gestionan clientes y unidades.

7.2. HU-002 — Creación de presupuestos estructurados

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero crear presupuestos con ítems globales e ítems de trabajo, para cotizar obras de forma estructurada y calcular totales automáticamente.

Criterios de aceptación:

- CA-1: Puedo agregar ítems globales (por ejemplo Recepción, Fachada, Departamentos).
- CA-2: Cada ítem global contiene ítems de trabajo con descripción, unidad, cantidad, precio unitario, precio total y peso de avance.
- CA-3: Cada ítem de trabajo tiene tipo de coeficiente (MO, Materiales, Construcción).
- CA-4: El sistema recalcula totales de ítem global y presupuesto al modificar cantidades o precios.
- CA-5: Puedo adjuntar documentación administrativa al presupuesto.

7.3. HU-003 — Duplicación de presupuestos

Prioridad: Media · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero duplicar un presupuesto existente, para agilizar la confección de nuevas propuestas comerciales.

Criterios de aceptación:

- CA-1: Puedo duplicar un presupuesto desde el listado o el detalle.
- CA-2: La copia incluye estructura de ítems globales, ítems de trabajo, cantidades y configuración técnica.
- CA-3: El presupuesto duplicado inicia en estado Borrador con nueva fecha de emisión.
- CA-4: Puedo modificar cliente, cantidades y valores en la copia sin afectar el original.

7.4. HU-004 — Coeficientes y confirmación de presupuesto

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero aplicar coeficientes de actualización y confirmar presupuestos, para reflejar inflación, cerrar la negociación y generar los certificados base de la obra.

Criterios de aceptación:

- CA-1: Puedo cambiar el estado del presupuesto: Borrador → Enviado → En Revisión → Aprobado / Rechazado → Confirmado.
- CA-2: Al aplicar coeficientes, solo se actualizan ítems según su tipo (MO, Materiales, Construcción).
- CA-3: El sistema guarda historial de cada ajuste con fecha y valores anteriores y nuevos.
- CA-4: Al confirmar, se generan automáticamente certificado de obra y certificado administrativo.
- CA-5: No puedo confirmar un presupuesto sin estar en estado Aprobado.

7.5. HU-005 — Asignación de tareas a obradores

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero asignar tareas a obradores con fechas y prioridad, para planificar la ejecución de la obra según el presupuesto confirmado.

Criterios de aceptación:

- CA-1: Puedo crear tareas vinculadas a ítems de trabajo del presupuesto confirmado.
- CA-2: Cada tarea tiene fecha de inicio, fecha estimada, prioridad y obrero responsable.
- CA-3: El obrero ve solo sus tareas asignadas en su vista.
- CA-4: Puedo filtrar tareas por obra, obrero y estado.

7.6. HU-006 — Registro de avances por obrero

Prioridad: Alta · Stakeholder: STK-03 (Obrador)

Como Obrador, quiero registrar avances con porcentaje, cantidades y evidencia fotográfica, para documentar el trabajo realizado y habilitar su validación.

Criterios de aceptación:

- CA-1: Puedo registrar avance diario, semanal o quincenal según configuración de la obra.
- CA-2: Cada registro incluye porcentaje completado, cantidades ejecutadas y observaciones.
- CA-3: Puedo adjuntar una o más fotografías como evidencia.
- CA-4: El avance queda en estado Pendiente de validación hasta aprobación del administrador.
- CA-5: La interfaz es usable desde dispositivo móvil (responsive).

7.7. HU-007 — Validación de avances y certificación quincenal

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero validar avances y generar la certificación quincenal, para habilitar pagos a obradores y actualizar el avance de la obra.

Criterios de aceptación:

- CA-1: Puedo aprobar o rechazar avances con comentarios al obrero.
- CA-2: El sistema calcula avance ponderado a nivel ítem, ítem global y obra.
- CA-3: Cada quince días se consolida certificación quincenal con trabajos ejecutados e importe a pagar.
- CA-4: Al aprobar avances, se actualizan indicadores de avance físico de la obra.
- CA-5: El obrero puede consultar historial de pagos y montos pendientes de liberación.

7.8. HU-008 — Validación de certificado administrativo por arquitecto

Prioridad: Alta · Stakeholder: STK-04 (Arquitecto)

Como Arquitecto, quiero revisar y aprobar o rechazar certificados administrativos mensuales, para validar el avance contractual de la obra frente al cliente.

Criterios de aceptación:

- CA-1: Veo certificados mensuales con avance del período y avance acumulado.
- CA-2: Puedo Aprobar o Solicitar Revisión con observaciones escritas.
- CA-3: Al solicitar revisión, el administrador ajusta y genera nueva versión numerada.
- CA-4: El historial conserva todas las versiones del certificado.
- CA-5: Los avances quincenales alimentan automáticamente el certificado administrativo mensual.

7.9. HU-009 — Generación de órdenes de pago

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero generar órdenes de pago desde certificados administrativos aprobados, para facturar al cliente de forma trazable y con importes correctos.

Criterios de aceptación:

- CA-1: Solo se genera orden de pago si el certificado mensual está aprobado por el arquitecto.
- CA-2: La orden incluye cliente, obra, certificado, importe, IVA, impuestos, neto y fecha de vencimiento.
- CA-3: Puedo visualizar y exportar la orden en formato imprimible.
- CA-4: La orden queda vinculada al certificado que la originó.

7.10. HU-010 — Registro de cobranzas

Prioridad: Alta · Stakeholder: STK-06 (Finanzas)

Como Administrador, quiero registrar cobranzas con distintos medios de pago, para controlar ingresos y estados de cada orden de pago.

Criterios de aceptación:

- CA-1: Medios de pago configurables: transferencia, cheque, e-cheq, efectivo, otros.
- CA-2: Estados de cobranza: Pendiente, Parcial, Cobrado, Vencido.
- CA-3: Puedo registrar pagos parciales y el saldo pendiente se actualiza.
- CA-4: El administrador confirma la recepción del pago en el sistema.
- CA-5: Según el medio de pago, se aplican o no ciertos impuestos (configurable).

7.11. HU-011 — Gestión de jornales a obradores

Prioridad: Alta · Stakeholder: STK-02 (Administrador)

Como Administrador, quiero gestionar obligaciones y pagos quincenales de jornales, para controlar egresos a obradores y contratistas.

Criterios de aceptación:

- CA-1: Cada quince días se generan obligaciones de pago derivadas de la certificación quincenal.
- CA-2: Puedo registrar pagos parciales y pagos completos.
- CA-3: El historial financiero por obrero muestra liquidaciones y saldos.
- CA-4: Los pagos al obrero se sincronizan con el certificado de obra aprobado.

7.12. HU-012 — Dashboard ejecutivo con KPIs

Prioridad: Alta · Stakeholder: STK-01 (Director)

Como Director, quiero visualizar un dashboard con KPIs financieros y operativos, para tomar decisiones sobre rentabilidad, flujo de fondos y estado de las obras.

Criterios de aceptación:

- CA-1: Vista empresa: facturación total, cobrado pendiente, egresos, rentabilidad, flujo de fondos.
- CA-2: Vista unidad de negocio: resultado económico, obras activas, certificados emitidos.
- CA-3: Vista obra: avance físico, avance financiero, pagos recibidos y realizados, rentabilidad estimada.
- CA-4: Mínimo seis KPIs financieros y cuatro operativos visibles con datos actualizados.
- CA-5: Puedo filtrar por período y unidad de negocio.

8. Índice del Product Backlog (referencia para tablero Kanban)

Ítems a incorporar en la columna Product Backlog del tablero (punto 5 y siguientes):

1. HU-001 — Clientes y unidades de negocio
2. HU-002 — Presupuestos estructurados
3. HU-003 — Duplicación de presupuestos
4. HU-004 — Coeficientes y confirmación
5. HU-005 — Asignación de tareas a obradores
6. HU-006 — Registro de avances (Obrador)
7. HU-007 — Validación y certificación quincenal
8. HU-008 — Certificado administrativo (Arquitecto)
9. HU-009 — Órdenes de pago
10. HU-010 — Registro de cobranzas
11. HU-011 — Jornales quincenales
12. HU-012 — Dashboard ejecutivo

Agrupación prevista por milestone (detalle en punto 6 del TP): HU-001 a HU-004 (M1), HU-005 a HU-008 (M2), HU-009 a HU-012 (M3).

9. Control de versión

v0.4.0 (2026-06-17) — Análisis de 20 RF, 8 RNF, 10 RN, 12 historias de usuario con criterios de aceptación y trazabilidad al flujo de negocio.
