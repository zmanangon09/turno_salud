# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 04

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-20                                        |
| **Hora inicio**        | 10:00                                                    | **Hora cierre**  | 10:45                                             |
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

1. Lectura y aprobación del Acta 03.
2. Presentación del Enunciado del trabajo revisado y de sus supuestos.
3. Acuerdo de las instrucciones de entrega (GP.1.2).
4. Revisión del Plan del proyecto verificado (GP.1.14).
5. Aceptación del plan.

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 03

Resumen de lo discutido: se leyó el Acta 03 (2026-11-19, 18:30–19:45), que registra la verificación del plan por el equipo. No hubo observaciones.

### Punto 2: Enunciado del trabajo revisado y supuestos

Resumen de lo discutido: Zaith (GP) presentó los seis vacíos detectados en el Enunciado y cómo se resolvieron: alcance incluido y excluido, cuatro perfiles de usuario, entregables, criterios de aceptación, supuestos técnicos (sección 2.9) y representante del cliente. El CL confirmó los supuestos marcados en el documento, incluida la exclusión de la historia clínica, los pagos en línea, la app móvil nativa, los SMS/WhatsApp y la telemedicina.

### Punto 3: Instrucciones de entrega (GP.1.2)

Resumen de lo discutido: se revisó la tabla de la sección 2.6 del Enunciado. El CL acordó los cinco entregables, sus semanas y la forma de entrega:

| Entregable | Semana | Forma de entrega | Aprueba |
|------------|--------|------------------|---------|
| E1. Plan del proyecto | 2 | Repositorio GitHub y reunión con el CL | CL |
| E2. Especificación de requisitos | 3 | Repositorio GitHub y acta de validación | CL |
| E3. Arquitectura y diseño detallado | 5 | Repositorio GitHub | LT y GP |
| E4. Versión beta e informe de pruebas | 10 | Servidor de pruebas (staging) e informe en GitHub | RP, LT y validación del CL |
| E5. Configuración de software y cierre | 12 | Versión `v1.0.0` en GitHub, sistema en producción y Acta de aceptación | CL |

Se acordó además que cada entregable se envía al CL con al menos 48 horas de anticipación a la reunión en la que se revisa.

### Punto 4: Revisión del Plan del proyecto

Resumen de lo discutido: Zaith presentó el plan verificado: descomposición por procesos, estimación PERT de 1 148 horas-persona, calendario de 12 semanas con sus hitos, presupuesto de USD 17 044 frente al tope de USD 18 000 y los nueve riesgos con sus respuestas. Matías explicó la mitigación del riesgo de cruce de horarios (R2) y las reglas del repositorio. El CL pidió que cualquier cambio de funciones después de validar los requisitos (E2) se tramite como solicitud de cambio, con su efecto en horas y costo, tal como indica la sección 3.14 del plan. No pidió cambios al plan.

### Punto 5: Aceptación del plan

Resumen de lo discutido: el CL aceptó el Plan del proyecto, versión 1.0, como línea base del proyecto. El plan pasa al estado **Aceptado** y con él se cierra la tarea GP.1 de planificación.

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 03 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Confirmar los supuestos del Enunciado del trabajo revisado (versión 1.1)                   | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | Acordar las instrucciones de entrega de E1 a E5 (GP.1.2)                                   | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | **Aceptar** el Plan del proyecto, versión 1.0, como línea base (GP.1.14)                   | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Marcar el plan como aceptado y etiquetar `E1-v1.0` en el repositorio       | Zaith (GP)    | 2026-11-20   |
| Actualizar el estado de las tareas en el README                            | Zaith (GP)    | 2026-11-20   |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-20   |

---

## Cierre

- **Hora de cierre:** 10:45
- **Próxima reunión:** por convocar. Revisión del plan con todo el equipo al iniciar la implementación (IS.1.1).

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
