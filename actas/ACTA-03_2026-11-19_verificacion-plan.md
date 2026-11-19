# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 03

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-19                                        |
| **Hora inicio**        | 18:30                                                    | **Hora cierre**  | 19:45                                             |
| **Órgano reunido**     | Equipo de trabajo (ET) de la VSE                         | **Modalidad**    | [ ] Presencial  [x] Virtual  [ ] Mixta            |
| **Lugar / Plataforma** | Google Meet                                              |                  |                                                   |

---

## Asistentes y quórum

- **Quórum requerido presente:** [x] Sí  [ ] No
- **Miembros presentes:** 4 de 4

### Asistentes

| Nombre    | Cargo (rol ISO/IEC 29110)                       |
|-----------|-------------------------------------------------|
| Zaith Manangón | Gestor del proyecto (GP)                       |
| Matías Lugmaña | Líder técnico (LT) y Programador (PR)           |
| Alexander Villacres | Analista (AN) y Diseñador (DIS)                 |
| Andrea Raura | Responsable de pruebas (RP) y Programadora (PR). Organizadora y secretaria |

**Ausentes:** Ninguno

**Invitados:** Ninguno. La revisión con el cliente (CL) se hará en una reunión aparte (Acta 04).

---

## Orden del día

1. Lectura y aprobación del Acta 02.
2. Presentación del Plan del proyecto, versión 1.0.
3. Verificación del plan con el equipo (GP.1.13).
4. Revisión del Enunciado del trabajo: sección de supuestos técnicos.
5. Preparación de la reunión con el cliente (GP.1.14).

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 02

Resumen de lo discutido: se leyó el Acta 02 (2026-11-18, 18:30–20:00), que registra la revisión del Enunciado, la propuesta de instrucciones de entrega y la distribución del trabajo para el plan. No hubo observaciones.

### Punto 2: Presentación del Plan del proyecto

Resumen de lo discutido: Zaith (GP) presentó `03-plan-proyecto/plan-proyecto.md`, versión 1.0, con sus 17 secciones. Los datos principales del plan:

| Dato | Valor |
|------|-------|
| Esfuerzo estimado con PERT | 1 148 horas-persona |
| Horas por integrante | Zaith 176 · Matías 352 · Alexander 319 · Andrea 301 |
| Utilización de la capacidad | 59,8 % (4 personas × 40 h × 12 semanas = 1 920 h) |
| Calendario | GP.1 en S1–S2, IS.2 en S2–S3, IS.3 en S3–S5, IS.4 en S5–S10, IS.5 en S8–S11, IS.6 en S11–S12 |
| Presupuesto | Trabajo USD 14 227 + servicios USD 547 + reserva USD 2 270 = **USD 17 044** (margen USD 956) |
| Riesgos | 9 riesgos identificados (R1 a R9), cada uno con respuesta y responsable |

### Punto 3: Verificación del plan (GP.1.13)

Resumen de lo discutido: cada integrante revisó con más detalle una parte del plan:

- **Zaith:** recalculó las ocho estimaciones PERT y comprobó que las horas cuadran entre 3.5, 3.6 y 3.10 y que el presupuesto no pasa de USD 18 000.
- **Matías:** comprobó la alineación con el Enunciado, los recursos técnicos, los riesgos técnicos y las reglas del repositorio.
- **Alexander:** revisó IS.2, IS.3 y el orden del calendario.
- **Andrea:** revisó las tareas de verificación y validación de cada proceso, la carga de las semanas S8 a S10 y los hitos.

Se registraron cinco observaciones y todas se corrigieron durante la reunión. Los ocho puntos de la lista de verificación se cumplen. El detalle está en `03-plan-proyecto/resultados-verificacion-plan.md`.

### Punto 4: Supuestos técnicos del Enunciado

Resumen de lo discutido: Matías (LT) señaló que la tabla de observaciones del Enunciado remitía a una sección 2.9 de supuestos técnicos que no se había escrito. Se agregó la sección 2.9 con los supuestos de arquitectura, navegadores, alojamiento, correo, datos que se guardan, protección de datos y zona horaria. El Enunciado pasa a la versión 1.1.

### Punto 5: Preparación de la reunión con el cliente

Resumen de lo discutido: se acordó presentar al docente (CL) el plan verificado en la próxima clase. Zaith expondrá el plan y las instrucciones de entrega (E1 a E5); Matías responderá las preguntas técnicas y Andrea tomará el acta.

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 02 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Dar por **verificado** el Plan del proyecto, versión 1.0, con las cinco observaciones corregidas | [x] Unanimidad  [ ] Mayoría  [ ] Otras |
| 3 | Agregar la sección 2.9 de supuestos técnicos al Enunciado (versión 1.1)                    | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | Presentar el plan verificado al cliente para su aceptación (GP.1.14)                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Subir al repositorio el plan verificado y los resultados de verificación   | Zaith (GP)    | 2026-11-19   |
| Subir la sección 2.9 del Enunciado                                          | Matías (LT)   | 2026-11-19   |
| Preparar la presentación del plan para el cliente                          | Zaith (GP)    | 2026-11-20   |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-19   |

---

## Cierre

- **Hora de cierre:** 19:45
- **Próxima reunión:** 2026-11-20, 10:00, presencial (ESPE, aula de clase). Revisión y aceptación del Plan del proyecto con el cliente (Acta 04).

---

## Firmas y aprobación

| Organizadora y secretaria |
|---------------------------|
| Firma: ________________   |
| Nombre: Andrea Raura      |

| Asistente | Rol            | Firma            |
|-----------|----------------|------------------|
| Zaith Manangón | GP             | ________________ |
| Matías Lugmaña | LT, PR         | ________________ |
| Alexander Villacres | AN, DIS        | ________________ |
| Andrea Raura | RP, PR         | ________________ |

**Aprobado en sesión del:** 2026-11-20 (Acta 04)
