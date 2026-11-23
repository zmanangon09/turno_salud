# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 07

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-23 (semana 5 del proyecto)                |
| **Hora inicio**        | 11:30                                                    | **Hora cierre**  | 12:30                                             |
| **Órgano reunido**     | Equipo de trabajo (ET) de la VSE y Cliente (CL)          | **Modalidad**    | [x] Presencial  [ ] Virtual  [ ] Mixta            |
| **Lugar / Plataforma** | ESPE, campus Sangolquí (aula de clase)                   |                  |                                                   |

---

## Asistentes y quórum

- **Quórum requerido presente:** [x] Sí  [ ] No
- **Miembros presentes:** 4 de 4 del equipo, más el cliente

### Asistentes

| Nombre    | Cargo (rol ISO/IEC 29110)                       |
|-----------|-------------------------------------------------|
| Zaith Manangón | Gestor del proyecto (GP)                       |
| Matías Lugmaña | Líder técnico (LT) y Programador (PR)           |
| Alexander Villacres | Analista (AN) y Diseñador (DIS)                 |
| Andrea Raura | Responsable de pruebas (RP) y Programadora (PR). Secretaria |
| Docente de la asignatura | Cliente (CL), en representación de la clínica |

**Ausentes:** Ninguno

---

## Orden del día

1. Lectura y aprobación del Acta 06.
2. Avance del proyecto a la semana 5 (GP.2.4).
3. Solicitud de cambio SC-01: lista de espera.
4. Solicitud de cambio SC-02: recordatorios por WhatsApp.
5. Actualización del plan y de los documentos afectados.

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 06

Resumen de lo discutido: se leyó el Acta 06, que registra la validación de la Especificación de requisitos (E2). Sin observaciones.

### Punto 2: Avance a la semana 5

Resumen de lo discutido: Zaith (GP) informó que E1 y E2 se entregaron a tiempo y que E3 (arquitectura y diseño) quedó verificado esta semana, como dice el calendario. La construcción empezó con autenticación y catálogos. Horas reales acumuladas: 3 % por encima de lo planificado, dentro del umbral de 10 % del plan (3.16).

### Punto 3: SC-01, lista de espera

Resumen de lo discutido: el CL presentó formalmente la lista de espera que había anticipado en la validación (V-05). Zaith y Matías (LT) presentaron la evaluación: 54 horas-persona, USD 647, sin cambio de hitos y pagada con la reserva del riesgo R1. Advirtieron que Matías, Alexander y Andrea quedan en 40 h en varias semanas de S6 a S10, lo que deja poca holgura. Se ofrecieron tres opciones: incluirla completa, una versión reducida con llamada manual de recepción, o diferirla. El CL eligió incluirla completa (opción A). Detalle en la ficha [SC-01](../05-solicitudes-cambio/SC-01_lista-de-espera.md).

### Punto 4: SC-02, recordatorios por WhatsApp

Resumen de lo discutido: el CL preguntó si los recordatorios podían enviarse también por WhatsApp. Zaith recordó que esta función está excluida en el Enunciado (2.5) y que el CL confirmó esa exclusión en el Acta 04. Matías explicó que requiere un proveedor externo con costo por mensaje y unas 40 horas que, después de SC-01, no caben sin mover hitos ni dejar la reserva por debajo de los riesgos pendientes. El CL aceptó no incluirla y dejarla como mejora futura. Detalle en la ficha [SC-02](../05-solicitudes-cambio/SC-02_notificaciones-whatsapp.md).

### Punto 5: Actualización del plan y los documentos

Resumen de lo discutido: con SC-01 aceptada se actualizan el Plan del proyecto (v1.1, sección 3.18), la Especificación de requisitos (v1.1), el Enunciado del trabajo (v1.2) y el diseño (E3 v1.1). El presupuesto total no cambia (USD 17 044): USD 647 pasan de la reserva al trabajo del equipo.

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 06 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | **Aceptar** SC-01 (opción A), con USD 647 de la reserva para contingencias                 | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | **Rechazar** SC-02 para la versión 1.0 y anotarla como mejora futura                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | Aprobar el Plan del proyecto v1.1 como nueva línea base                                    | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Actualizar el plan a v1.1 y el registro de solicitudes de cambio           | Zaith (GP)    | S5           |
| Agregar RF-19, RN-08 y P-10 a la especificación (v1.1) y revalidarla con el CL | Alexander (AN) | S6       |
| Actualizar el diseño (E3 v1.1) y verificar la parte cambiada               | Matías (LT) y Alexander (DIS) | S7 |
| Diseñar CP-25 y las pruebas de regresión de RF-10 a RF-12                  | Andrea (RP)   | S8           |
| Vigilar cada lunes la carga de S6 a S10 (riesgo R4)                        | Zaith (GP)    | S10          |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-23   |

---

## Cierre

- **Hora de cierre:** 12:30
- **Próxima reunión:** reunión quincenal con el CL en S7.

---

## Firmas y aprobación

| Cliente (CL)              | Secretaria                |
|---------------------------|---------------------------|
| Firma: ________________   | Firma: ________________   |
| Nombre: Docente de la asignatura | Nombre: Andrea Raura |

| Asistente | Rol            | Firma            |
|-----------|----------------|------------------|
| Zaith Manangón | GP             | ________________ |
| Matías Lugmaña | LT, PR         | ________________ |
| Alexander Villacres | AN, DIS        | ________________ |
| Andrea Raura | RP, PR         | ________________ |

**Aprobado en sesión del:** pendiente (próxima reunión)
