# VSE de Sangolquí — Proyecto TurnoSalud

ESPE · Aseguramiento de la Calidad de Software · **Grupo 6** · Caso «TurnoSalud» (ISO/IEC 29110, Perfil Básico)

## ACTA DE REUNIÓN No. 08

| Campo                  | Valor                                                    | Campo            | Valor                                             |
|------------------------|----------------------------------------------------------|------------------|---------------------------------------------------|
| **Tipo de reunión**    | [x] Ordinaria  [ ] Extraordinaria                        | **Fecha**        | 2026-11-23 (semana 12 del proyecto)               |
| **Hora inicio**        | 13:00                                                    | **Hora cierre**  | 14:15                                             |
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

1. Lectura y aprobación del Acta 07.
2. Comprobación de los criterios de aceptación.
3. Medición del retrabajo (GP.3.1) y ratificación de la acción correctiva AC-01 (GP.3.2).
4. Plazo, costo, riesgos y solicitudes de cambio.
5. Entrega de la configuración de software (E5) y aceptación (GP.4.1).
6. Lecciones aprendidas y actualización del repositorio (GP.4.2).

---

## Desarrollo de la reunión

### Punto 1: Lectura y aprobación del Acta 07

Resumen de lo discutido: se leyó el Acta 07 (solicitudes de cambio SC-01 y SC-02). Andrea (RP) confirmó que SC-01 quedó implementada y probada en S11: CP-25 y la regresión de RF-10 a RF-12 pasaron. Sin observaciones.

### Punto 2: Criterios de aceptación

Resumen de lo discutido: Andrea presentó los resultados de los seis criterios del Enunciado (2.8). El CL repitió en producción la reserva de un turno (4 pasos, 1 min 10 s) y la lista de espera: se anotó, canceló otro turno desde una segunda cuenta y recibió el aviso por correo. Los seis criterios se cumplen. Quedan 2 defectos menores abiertos (D-72 y D-73), que el CL acepta para corregir en mantenimiento.

### Punto 3: Medición del retrabajo

Resumen de lo discutido: Zaith (GP) presentó la [Medición del retrabajo](../06-retrabajo-cierre/medicion-retrabajo.md): 1 254 h reales, de las cuales 182 fueron retrabajo, es decir **14,5 %**, frente a 18 % del caso BitPerfect. Se aclaró que las 54 h de SC-01 no cuentan como retrabajo porque son trabajo nuevo pedido por el cliente. Andrea mostró que los defectos encontrados en requisitos y diseño costaron 1,8 h cada uno y los encontrados en pruebas finales 3,5 h. El equipo ratificó la acción correctiva AC-01 de S8 (reasignación de 8 h a Alexander y pruebas de concurrencia adelantadas), que llevó a IS.4 de +11 % a +5,6 %.

### Punto 4: Plazo, costo, riesgos y cambios

Resumen de lo discutido: el proyecto terminó en las 12 semanas, con un solo hito interno atrasado una semana. Costo real USD 16 029 frente al tope de USD 18 000; de la reserva se usaron USD 1 255 (SC-01 y horas sobre el plan) y quedan USD 1 971 sin gastar. R1, R2, R4 y R9 ocurrieron total o parcialmente y se atendieron con las respuestas del plan. Detalle en el [Informe de cierre](../06-retrabajo-cierre/informe-cierre.md).

### Punto 5: Entrega y aceptación

Resumen de lo discutido: Matías (LT) entregó la configuración de software según las instrucciones de E5: versión `v1.0.0`, sistema en producción, manuales y guías. Las credenciales de administrador se entregaron en persona. El CL revisó la lista de verificación de entrega y **firmó el registro de aceptación** (sección 6.15 del informe de cierre).

### Punto 6: Lecciones aprendidas y repositorio

Resumen de lo discutido: el equipo acordó las lecciones de la sección 6.16 del informe de cierre. Las principales: llevar completas al diseño las reglas de «no cruce», no aceptar cambios que dejen a alguien por encima de 36 h por semana y fijar una meta de retrabajo de 12 % o menos desde el plan. Zaith actualiza el repositorio y el README para cerrar el proyecto.

---

## Decisiones y votaciones

| # | Decisión                                                                                   | Votación                                   |
|---|--------------------------------------------------------------------------------------------|--------------------------------------------|
| 1 | Aprobar el Acta 07 sin observaciones                                                       | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 2 | Ratificar la acción correctiva AC-01 y el uso de USD 608 de la reserva                     | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 3 | Aceptar los defectos menores D-72 y D-73 para corregir en mantenimiento                    | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |
| 4 | **Aceptar** el producto TurnoSalud `v1.0.0` y **cerrar** el proyecto (GP.4.1)              | [x] Unanimidad  [ ] Mayoría  [ ] Otras     |

---

## Compromisos y tareas

| Compromiso / Tarea                                                         | Responsable   | Fecha límite |
|----------------------------------------------------------------------------|---------------|--------------|
| Actualizar el repositorio y el README con el cierre (GP.4.2)               | Zaith (GP)    | 2026-11-23   |
| Hacer el respaldo final del repositorio y de la base de datos              | Matías (LT)   | 2026-11-23   |
| Registrar esta acta en el repositorio                                      | Andrea        | 2026-11-23   |

---

## Cierre

- **Hora de cierre:** 14:15
- **Próxima reunión:** ninguna. Proyecto cerrado.

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

**Aprobado en sesión del:** 2026-11-23 (última reunión del proyecto; aprobada al cierre por los asistentes)
