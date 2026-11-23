# 4. Especificación de requisitos de software — AN

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsable:** Alexander Villacres (AN/DIS) · **Apoyo:** Matías Lugmaña (LT), Andrea Raura (RP) y Zaith Manangón (GP)
**Tareas de la norma:** IS.2.1 Asignar tareas · IS.2.2 Documentar la Especificación de requisitos · IS.2.3 Verificarla · IS.2.4 Validarla con el cliente · IS.2.7 Incorporarla a la configuración de software
**Productos de entrada:** [Enunciado del trabajo revisado](../02-enunciado-trabajo/enunciado-trabajo.md) · [Plan del proyecto aceptado](../03-plan-proyecto/plan-proyecto.md)
**Semana del proyecto:** S2 y S3 · **Entregable:** E2
**Versión:** 1.1 · **Estado:** Validado ([Verificación](resultados-verificacion-requisitos.md) · [Validación](resultados-validacion-requisitos.md)) · Cambio aprobado: [SC-01](../05-solicitudes-cambio/SC-01_lista-de-espera.md)

---

## 4.1 Propósito

Este documento dice qué debe hacer TurnoSalud y con qué calidad. Es la base para el diseño (IS.3), la construcción (IS.4) y las pruebas (IS.5), y es contra lo que el cliente acepta el producto al final. Todo requisito tiene un identificador para poder seguirlo hasta su caso de prueba.

Las tareas IS.2.5 e IS.2.6 (versión preliminar del manual de usuario) no se hacen en esta etapa: el Plan del proyecto (3.3) deja los manuales en IS.6.

## 4.2 Fuentes de los requisitos (IS.2.2)

| Fuente | Qué aportó |
|--------|-----------|
| Enunciado del trabajo revisado (2.4, 2.5, 2.8 y 2.9) | Usuarios, alcance incluido y excluido, criterios de aceptación y supuestos técnicos confirmados por el CL en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md). |
| Taller interno de elucidación (S2) | Recorrido de un día de trabajo de cada usuario (paciente, recepción, médico, administrador) para encontrar las funciones que el enunciado no detallaba. |
| Revisión de prototipos con el CL ([Acta 06](../actas/ACTA-06_2026-11-23_validacion-requisitos.md)) | Reglas de negocio que solo podía definir la clínica: plazo para cancelar, pacientes sin correo y filtros del reporte. |
| Solicitud de cambio SC-01 ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md)) | Lista de espera (RF-19, RN-08), agregada en la versión 1.1. |

## 4.3 Usuarios y permisos

| Función | Paciente | Recepción | Médico | Administrador |
|---------|:--------:|:---------:|:------:|:-------------:|
| Registrarse e iniciar sesión | ✓ | ✓ | ✓ | ✓ |
| Consultar disponibilidad y reservar | ✓ | ✓ (a nombre del paciente) | | |
| Anotarse en la lista de espera (v1.1) | ✓ | ✓ (a nombre del paciente) | | |
| Reprogramar y cancelar | ✓ (hasta 4 h antes) | ✓ (hasta la hora del turno) | | |
| Ver agenda del día y registrar llegada | | ✓ | | |
| Ver su agenda y marcar atendido / no asistió | | | ✓ | |
| Registrar ausencias | | | ✓ | ✓ |
| Gestionar especialidades, médicos, consultorios y horarios | | | | ✓ |
| Gestionar cuentas internas y ver reportes | | | | ✓ |

## 4.4 Requisitos funcionales

Prioridad: **Alta** = sin esto no se acepta el producto · **Media** = se entrega en v1.0, pero puede negociarse si hay retraso.

| ID | Requisito | Usuario | Prioridad | Criterio de aceptación |
|----|-----------|---------|-----------|------------------------|
| RF-01 | Registro de paciente con cédula, nombres, apellidos, fecha de nacimiento, correo y teléfono. | Paciente | Alta | No acepta una cédula o un correo ya registrados; la cuenta se activa al abrir el enlace de confirmación enviado al correo. |
| RF-02 | Inicio de sesión, cierre de sesión y recuperación de contraseña. | Todos | Alta | El enlace de recuperación vence a los 30 minutos y solo se puede usar una vez. |
| RF-03 | Control de acceso por rol. | Todos | Alta | Cada usuario ve y puede usar solo las funciones de su rol (4.3); la API rechaza con error 403 cualquier otra petición. |
| RF-04 | Gestión de especialidades (crear, editar y desactivar), con la duración del turno de cada una. | Administrador | Alta | Una especialidad desactivada deja de aparecer al reservar, pero sus turnos ya reservados se mantienen. |
| RF-05 | Gestión de médicos y consultorios; un médico puede tener una o más especialidades. | Administrador | Alta | No se puede desactivar un médico con turnos futuros sin antes reprogramarlos o cancelarlos. |
| RF-06 | Horario base semanal de cada médico (día, hora de inicio y fin, consultorio) y registro de ausencias. | Administrador, Médico | Alta | Al registrar una ausencia que choca con turnos ya reservados, el sistema lista esos turnos y avisa a recepción para reprogramarlos. |
| RF-07 | Consultar disponibilidad por especialidad, médico (o «cualquier médico disponible») y fecha, hasta 30 días hacia adelante. | Paciente, Recepción | Alta | Solo se muestran bloques libres, dentro del horario del médico y fuera de sus ausencias. |
| RF-08 | Reservar un turno. | Paciente, Recepción | Alta | La reserva se completa en 4 pasos como máximo (4.7) y el turno queda en estado «Reservado». |
| RF-09 | Impedir cruces de horario. | Sistema | Alta | Un médico no puede tener dos turnos en el mismo bloque y un consultorio no puede tener dos turnos al mismo tiempo, aun si dos usuarios reservan a la vez. |
| RF-10 | Reprogramar un turno. | Paciente, Recepción | Alta | Cumple RN-03; el bloque anterior queda libre en el mismo momento. |
| RF-11 | Cancelar un turno. | Paciente, Recepción | Alta | Cumple RN-03; el turno pasa a «Cancelado» y su bloque queda libre. |
| RF-12 | Notificaciones por correo de confirmación, reprogramación y cancelación, y recordatorio 24 h antes del turno. | Paciente | Alta | Las tres primeras llegan en menos de 5 minutos; el recordatorio se envía entre 24 y 23 h antes. |
| RF-13 | Registrar en recepción a pacientes que llegan o llaman, y reservar a su nombre. | Recepción | Alta | El correo es opcional en este registro (RN-06). |
| RF-14 | Agenda del día para recepción y registro de llegada del paciente. | Recepción | Alta | La agenda muestra los turnos del día por médico; al registrar la llegada el turno pasa a «En espera de atención». |
| RF-15 | Agenda diaria y semanal del médico; marcar el turno como atendido o no asistió. | Médico | Alta | El médico solo ve sus propios turnos (RN-05 para «no asistió»). |
| RF-16 | Gestión de cuentas internas (recepción, médico, administrador): crear, desactivar y restablecer contraseña. | Administrador | Alta | Una cuenta desactivada no puede iniciar sesión. |
| RF-17 | Reporte de turnos por rango de fechas, especialidad y médico: reservados, atendidos, cancelados y no asistió. | Administrador | Media | Los totales del reporte coinciden con los turnos de la base de datos para el mismo filtro. |
| RF-18 | «Mis turnos»: el paciente ve sus próximos turnos y su historial. | Paciente | Media | Desde esta pantalla puede reprogramar o cancelar los turnos que cumplan RN-03. |
| RF-19 | **Lista de espera (SC-01, v1.1).** Si no hay horarios libres en la especialidad y fecha buscadas, el paciente puede anotarse; cuando se cancela o reprograma un turno de esa especialidad y fecha, el sistema avisa por correo a los pacientes anotados. | Paciente, Recepción | Media | El aviso sale en menos de 5 minutos después de liberarse el bloque, en el orden de inscripción; el bloque se asigna al primero que reserva (RN-08). |

## 4.5 Reglas de negocio

| ID | Regla |
|----|-------|
| RN-01 | La duración del turno la define cada especialidad: 20 minutos por defecto, configurable entre 15 y 60. |
| RN-02 | Un paciente no puede tener dos turnos activos que se solapen, ni más de un turno activo en la misma especialidad. |
| RN-03 | El paciente puede reprogramar o cancelar hasta 4 horas antes del turno; después, solo recepción puede hacerlo. |
| RN-04 | Un turno se reserva con un mínimo de 1 hora y un máximo de 30 días de anticipación. |
| RN-05 | Si el paciente no llega 15 minutos después de la hora del turno, el médico o recepción pueden marcarlo como «no asistió». |
| RN-06 | Un paciente registrado por recepción sin correo no recibe notificaciones; recepción le entrega los datos del turno en el momento. |
| RN-07 | Todas las horas se manejan en la zona horaria de Ecuador continental (UTC-5). |
| RN-08 | **(SC-01)** Un paciente puede estar en la lista de espera de una sola fecha por especialidad. Su inscripción se borra cuando reserva un turno de esa especialidad o cuando pasa la fecha. El aviso no aparta el turno: lo obtiene quien reserve primero. |

## 4.6 Requisitos no funcionales

| ID | Tipo | Requisito | Cómo se comprueba |
|----|------|-----------|-------------------|
| RNF-01 | Usabilidad | Un paciente registrado reserva en 4 pasos como máximo y en menos de 2 minutos. | Prueba de usabilidad con el CL sobre el prototipo (IS.2.4) y sobre el sistema (IS.5). |
| RNF-02 | Rendimiento | La consulta de disponibilidad y la confirmación del turno responden en menos de 3 segundos con 50 usuarios simultáneos. | Prueba de carga en staging antes de E4. |
| RNF-03 | Compatibilidad | Funciona en las dos últimas versiones de Chrome, Edge, Firefox y Safari, en escritorio y en móvil desde 360 px de ancho. | Pruebas multinavegador (BrowserStack) y en distintas resoluciones. |
| RNF-04 | Seguridad | HTTPS en todo el sistema; contraseñas guardadas con bcrypt (costo 10 o más); la sesión vence tras 30 minutos sin actividad; la cuenta se bloquea 15 minutos después de 5 intentos fallidos. | Revisión de código en cada pull request y pruebas de seguridad en IS.5. |
| RNF-05 | Privacidad | Solo se guardan datos de identificación y contacto del paciente y datos del turno, nunca información clínica (LOPDP). | Revisión del modelo de datos en IS.3. |
| RNF-06 | Respaldo | Respaldo diario cifrado de la base de datos, guardado 30 días. | Restauración de prueba en staging. |
| RNF-07 | Idioma | Interfaz y mensajes de error en español, con texto que dice qué hacer para corregir el error. | Revisión de pantallas con el CL. |

## 4.7 Interfaz de usuario y prototipos

Prototipos de baja fidelidad hechos por Alexander (DIS) y recorridos con el CL en la validación:

| ID | Pantalla | Requisitos que cubre |
|----|----------|----------------------|
| P-01 | Registro, inicio de sesión y recuperación de contraseña | RF-01, RF-02 |
| P-02 | Buscar disponibilidad (especialidad, médico o «cualquier médico», fecha) | RF-07 |
| P-03 | Elegir horario | RF-07, RF-08 |
| P-04 | Confirmar turno | RF-08, RF-12 |
| P-05 | Mis turnos | RF-10, RF-11, RF-18 |
| P-06 | Agenda del día y registro de pacientes (recepción) | RF-13, RF-14 |
| P-07 | Agenda del médico | RF-15 |
| P-08 | Administración de especialidades, médicos, consultorios, horarios y cuentas | RF-04, RF-05, RF-06, RF-16 |
| P-09 | Reporte de turnos | RF-17 |
| P-10 | Anotarse en la lista de espera (desde P-03 cuando no hay horarios) — v1.1 | RF-19 |

**Flujo de reserva (RF-08, RNF-01):**

```
[1] Especialidad  →  [2] Médico o «cualquier médico» + fecha  →  [3] Horario libre  →  [4] Confirmar
```

En la prueba de usabilidad del prototipo, el CL completó la reserva en 4 pasos y en 1 min 20 s ([Resultados de validación](resultados-validacion-requisitos.md)).

## 4.8 Trazabilidad

Los casos de prueba (CP) se diseñan en IS.5; aquí se reserva su identificador para que cada requisito tenga al menos uno.

| Requisito | Alcance del Enunciado (2.5) | Prototipo | Criterio de aceptación (2.8) | Caso de prueba |
|-----------|-----------------------------|-----------|------------------------------|----------------|
| RF-01, RF-02, RF-03 | Registro, inicio de sesión y acceso por roles | P-01 | 1 | CP-01 a CP-03 |
| RF-04, RF-05, RF-06 | Catálogos y horarios | P-08 | 1 | CP-04 a CP-06 |
| RF-07, RF-08 | Agendamiento | P-02 a P-04 | 1, 3 | CP-07, CP-08 |
| RF-09 | Agendamiento sin cruces | — | 2 | CP-09 (incluye concurrencia) |
| RF-10, RF-11 | Reprogramación y cancelación | P-05 | 1 | CP-10, CP-11 |
| RF-12 | Notificaciones por correo | P-04 | 1 | CP-12 |
| RF-13, RF-14 | Panel de recepción | P-06 | 1 | CP-13, CP-14 |
| RF-15 | Panel de recepción y médicos | P-07 | 1 | CP-15 |
| RF-16, RF-17 | Vista administrativa | P-08, P-09 | 1 | CP-16, CP-17 |
| RF-18 | Agendamiento (paciente) | P-05 | 1 | CP-18 |
| RF-19 | Lista de espera (SC-01, Enunciado v1.2) | P-10 | 1 | CP-25 y regresión de CP-10 a CP-12 |
| RNF-01 | — | P-02 a P-04 | 3 | CP-19 |
| RNF-02 | — | — | 5 | CP-20 |
| RNF-03 | — | Todas | 4 | CP-21 |
| RNF-04, RNF-05, RNF-06 | Protección de datos (Enunciado 2.9) | — | — | CP-22 a CP-24 |

El criterio 6 (entrega de la configuración de software) no sale de un requisito del producto: se comprueba con la lista de verificación de IS.6.

## 4.9 Fuera de alcance

Se mantiene lo excluido en la sección 2.5 del Enunciado: historia clínica, pagos en línea y facturación electrónica, apps móviles nativas, notificaciones por SMS o WhatsApp y telemedicina. La solicitud de recordatorios por WhatsApp ([SC-02](../05-solicitudes-cambio/SC-02_notificaciones-whatsapp.md)) fue rechazada para esta versión. Cualquier función nueva después de esta validación se tramita como solicitud de cambio (riesgo R1 del plan).

## Historial de versiones

| Versión | Semana | Cambio | Aprobó |
|---------|--------|--------|--------|
| 0.1 | S2 | Primer borrador después del taller de elucidación | Alexander (AN) |
| 0.2 | S3 | Siete correcciones de la verificación interna (IS.2.3) | Equipo ([Acta 05](../actas/ACTA-05_2026-11-23_verificacion-requisitos.md)) |
| 1.0 | S3 | Cuatro correcciones de la validación con el cliente (IS.2.4) | CL ([Acta 06](../actas/ACTA-06_2026-11-23_validacion-requisitos.md)) |
| 1.1 | S6 | SC-01: RF-19, RN-08, P-10 y trazabilidad a CP-25; revalidado con el CL | CL ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md)) |

**Productos de trabajo:** Especificación de requisitos [verificada y validada] · Resultados de verificación · Resultados de validación · Registro de reunión (Actas 05 y 06). La versión 1.0 quedó en la configuración de software con la etiqueta `E2-v1.0` (IS.2.7); la versión 1.1, con `E2-v1.1`.
