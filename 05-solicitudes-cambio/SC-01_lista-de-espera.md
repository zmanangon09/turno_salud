# Solicitud de cambio SC-01 — Lista de espera

**Proyecto:** TurnoSalud · **Grupo 6**
**Tareas de la norma:** GP.2.2 Analizar y evaluar la solicitud de cambio (costo, calendario e impacto técnico) · GP.2.4 Revisar con el cliente y registrar el acuerdo · GP.3.3 Dar seguimiento al cambio hasta su cierre
**Roles:** GP y LT (evaluación) · CL (decisión)
**Registro:** [Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md) · [Registro de solicitudes de cambio](registro-solicitudes-cambio.md)
**Estado actual:** **Aceptada** e implementada

---

## 1. Datos de la solicitud

| Campo | Valor |
|-------|-------|
| **Identificador** | SC-01 |
| **Origen** | Cliente (observación V-05 de la [validación de requisitos](../04-requisitos/resultados-validacion-requisitos.md)) |
| **Solicitante y contacto** | Docente de la asignatura (CL), en representación de la clínica. Canal: reuniones quincenales y Zaith Manangón (GP) como punto de contacto |
| **Fecha de solicitud** | Semana 5 del proyecto (2026-11-23) |
| **Propósito del cambio** | Mejora. Cuando no hay horarios libres en la especialidad y fecha que busca, el paciente puede anotarse en una lista de espera. Si otro paciente cancela o reprograma un turno de esa especialidad y fecha, el sistema avisa por correo a los pacientes en espera, en el orden en que se anotaron; el primero que reserva se queda con el turno. |
| **Justificación del CL** | Hoy la clínica pierde turnos cancelados a última hora porque recepción no alcanza a llamar a otros pacientes. |
| **Sistema afectado** | TurnoSalud (único sistema). Módulos: agendamiento, cancelación y reprogramación, notificaciones por correo y base de datos. |
| **Impacto en la operación de sistemas existentes** | Ninguno en producción: TurnoSalud aún no está desplegado y la clínica no tiene otro sistema de turnos. Dentro del proyecto, el cambio toca la cancelación (RF-10, RF-11) y las notificaciones (RF-12), que ya están en construcción, por lo que hay riesgo de romperlas: se cubren con pruebas de regresión. |
| **Impacto en la documentación** | Especificación de requisitos → v1.1 (RF-19, RN-08, prototipo P-10) · Arquitectura y diseño (E3) → v1.1 (tabla `lista_espera` y flujo de aviso) · Plan del proyecto → v1.1 (sección 3.18) · Enunciado del trabajo → v1.2 (alcance) · Casos de prueba (CP-25) · Manual de usuario. |
| **Criticidad** | Media: es útil para la clínica, pero sin ella el sistema opera igual. |
| **Fecha requerida** | Con la entrega final E5 (semana 12). |

## 2. Historial de estados

| Estado | Semana | Quién | Qué pasó |
|--------|--------|-------|----------|
| **Propuesta** | S5 | CL | Presentó la solicitud en la reunión quincenal ([Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md)). |
| **Evaluada** | S5 | Zaith (GP) y Matías (LT) | Estimaron horas, costo, calendario e impacto técnico (sección 3). Se presentó al CL con tres opciones. |
| **Aceptada** | S5 | CL | Eligió la opción A, pagada con la reserva para contingencias del riesgo R1. |
| **Implementada y cerrada** | S11 | Andrea (RP) | Casos de prueba CP-25 y regresión de RF-10 a RF-12 aprobados; el CL la comprobó en la validación del sistema ([Informe de cierre](../06-retrabajo-cierre/informe-cierre.md)). |

## 3. Evaluación (GP.2.2)

### 3.1 Impacto técnico (Matías, LT)

- Se puede construir con la arquitectura actual: una tabla nueva `lista_espera` (paciente, especialidad, fecha, fecha de inscripción, estado) y un paso más en la transacción de cancelación y reprogramación que busca a quién avisar.
- Reutiliza el servicio de correo de RF-12; no requiere herramientas ni servicios nuevos.
- La inscripción se borra sola cuando el paciente reserva o cuando pasa la fecha.
- El riesgo principal es de regresión en la cancelación, que ya está construida; se mitiga con pruebas automáticas de RF-10 a RF-12 antes de fusionar.
- El diseño (E3) se verificó en S5, así que hay que actualizarlo y volver a verificar solo la parte cambiada.

### 3.2 Esfuerzo adicional por proceso

| Proceso | Trabajo | Zaith | Matías | Alexander | Andrea | Total (h) |
|---------|---------|-------|--------|-----------|--------|-----------|
| IS.2 Requisitos | RF-19, RN-08, prototipo P-10 y revalidación con el CL | 2 | | 6 | | 8 |
| IS.3 Diseño | Modelo de datos y flujo de aviso; verificación de lo cambiado | | 4 | 4 | | 8 |
| IS.4 Construcción | Backend (Matías) y pantallas (Andrea) con pruebas unitarias | | 14 | | 10 | 24 |
| IS.5 Pruebas | CP-25 y regresión de cancelación, reprogramación y notificaciones | | 2 | | 6 | 8 |
| IS.6 Entrega | Sección nueva del manual de usuario | | | 2 | | 2 |
| GP.2 Gestión | Evaluación, reunión con el CL y actualización del plan | 3 | 1 | | | 4 |
| **Total** | | **5** | **21** | **12** | **16** | **54** |

### 3.3 Costo (tarifas de la sección 3.10 del plan)

| Rol | Horas | Tarifa (USD/h) | Cálculo | Costo (USD) |
|-----|-------|----------------|---------|-------------|
| GP (Zaith) | 5 | 15 | 5 × 15 | 75 |
| AN/DIS (Alexander) | 12 | 12 | 12 × 12 | 144 |
| LT (Matías: diseño, pruebas y gestión) | 7 | 14 | 7 × 14 | 98 |
| PR (Matías: construcción) | 14 | 11 | 14 × 11 | 154 |
| PR (Andrea: construcción) | 10 | 11 | 10 × 11 | 110 |
| RP (Andrea: pruebas) | 6 | 11 | 6 × 11 | 66 |
| **Total** | **54** | | | **647** |

No hay costo de servicios: el plan de correo SMTP contratado cubre los avisos adicionales.

### 3.4 Calendario

Las 54 horas se reparten entre S5 y S11 sin mover ningún hito:

| Integrante | S5 | S6 | S7 | S8 | S9 | S10 | S11 | Carga máxima resultante |
|------------|----|----|----|----|----|-----|-----|-------------------------|
| Zaith      | +2 | +3 | | | | | | 14 h (S5) |
| Matías     | +1 | +4 | +4 | +4 | +2 | +4 | +2 | **40 h** (S6 a S8) |
| Alexander  | | +6 | +4 | | | | +2 | **40 h** (S6) |
| Andrea     | | | +4 | +2 | +2 | +2 | +6 | **40 h** (S8 a S10) |

Nadie pasa de 40 horas, pero Matías, Alexander y Andrea quedan al tope en varias semanas de construcción. La holgura del plan para absorber retrasos (3.7) casi desaparece de S6 a S10, así que sube la probabilidad del riesgo R4 (construcción subestimada). El GP lo vigila cada lunes.

### 3.5 Presupuesto

El cambio se paga con la reserva para contingencias, porque es justo el riesgo R1 previsto en el plan (cambios de requisitos después de E2, aporte de USD 800):

| Concepto | Plan v1.0 (USD) | Cambio | Plan v1.1 (USD) |
|----------|-----------------|--------|-----------------|
| Trabajo del equipo | 14 227 | + 647 | 14 874 |
| Servicios y herramientas | 547 | 0 | 547 |
| Reserva para contingencias | 2 270 | − 647 | 1 623 |
| **Total** | **17 044** | **0** | **17 044** |
| Tope del cliente | 18 000 | | 18 000 |

El presupuesto total no cambia y sigue por debajo del tope.

## 4. Opciones presentadas al cliente

| Opción | Qué incluye | Horas | Costo (USD) | Efecto |
|--------|-------------|-------|-------------|--------|
| **A. Incluir en v1.0** | Lista de espera con aviso automático por correo | 54 | 647 | Sin cambio de hitos; reserva baja a USD 1 623 y la carga de S6 a S10 queda al tope. |
| B. Versión reducida | El paciente se anota; recepción ve la lista y llama a mano | 22 | ≈ 270 | Menos riesgo, pero sigue dependiendo de que recepción llame a tiempo. |
| C. Diferir | Se deja para una versión posterior a la entrega | 0 | 0 | Sin efecto en el proyecto; la clínica sigue perdiendo turnos cancelados. |

## 5. Decisión (GP.2.4)

El CL eligió la **opción A**. Al afectar el alcance acordado, la decisión se negoció con el cliente y queda en el [Acta 07](../actas/ACTA-07_2026-11-23_solicitudes-cambio.md). Se actualizan el [Plan del proyecto](../03-plan-proyecto/plan-proyecto.md) a v1.1, la [Especificación de requisitos](../04-requisitos/especificacion-requisitos.md) a v1.1 y el [Enunciado del trabajo](../02-enunciado-trabajo/enunciado-trabajo.md) a v1.2.

**Aprobación:**

| Cliente (CL) | Gestor del proyecto (GP) | Líder técnico (LT) |
|--------------|--------------------------|--------------------|
| Firma: ________________ | Firma: ________________ | Firma: ________________ |
| Docente de la asignatura | Zaith Manangón | Matías Lugmaña |
