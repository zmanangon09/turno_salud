# Verificación de la Especificación de requisitos — IS.2.3

**Proyecto:** TurnoSalud · **Grupo 6**
**Documento revisado:** [Especificación de requisitos](especificacion-requisitos.md), versión 0.1
**Semana del proyecto:** S3 · **Fecha:** 2026-11-23 · **Registro:** [Acta 05](../actas/ACTA-05_2026-11-23_verificacion-requisitos.md)
**Resultado:** Especificación verificada (versión 0.2), lista para validar con el cliente

---

## Diferencia entre verificar y validar

- **Verificar (IS.2.3):** el equipo revisa que la especificación esté bien escrita: cada requisito es claro, se puede probar, no contradice a otro y sale del alcance acordado.
- **Validar (IS.2.4):** el cliente confirma que lo especificado es lo que la clínica necesita. Se hace después, con los prototipos ([Resultados de validación](resultados-validacion-requisitos.md)).

## Participantes

| Integrante          | Rol     | Qué revisó con más detalle |
|---------------------|---------|----------------------------|
| Alexander Villacres | AN, DIS | Autor. Presentó cada requisito y anotó las observaciones. |
| Matías Lugmaña      | LT, PR  | Que cada requisito se pueda construir con la arquitectura de la sección 2.9 del Enunciado; requisitos de seguridad y de cruce de horarios. |
| Andrea Raura        | RP, PR  | Que cada requisito tenga un criterio de aceptación que se pueda probar y un caso de prueba reservado en la trazabilidad (4.8). |
| Zaith Manangón      | GP      | Que nada quede fuera ni se agregue por encima del alcance incluido del Enunciado (2.5) y de los criterios de aceptación (2.8). |

## Lista de verificación

- [x] Cada requisito tiene identificador único (RF, RN, RNF).
- [x] Cada requisito está escrito sin ambigüedad: no usa palabras como «rápido», «fácil» o «seguro» sin una medida.
- [x] Cada requisito funcional tiene un criterio de aceptación que se puede probar.
- [x] Los requisitos no se contradicen entre sí.
- [x] Todo el alcance incluido del Enunciado (2.5) está cubierto por al menos un requisito.
- [x] Ningún requisito agrega funciones excluidas o no pedidas.
- [x] Los seis criterios de aceptación del Enunciado (2.8) están enlazados en la trazabilidad (4.8).
- [x] Los requisitos de seguridad y privacidad respetan los supuestos técnicos (2.9) y la LOPDP.
- [x] Cada pantalla del prototipo está enlazada a sus requisitos (4.7).

Los puntos se marcaron después de corregir las observaciones de la tabla siguiente.

## Observaciones

| # | Requisito | Observación | Corrección | Detectó | ¿Corregido? |
|---|-----------|-------------|------------|---------|-------------|
| 1 | RF-08 | Decía «reservar un turno de forma rápida»: no se puede probar. | Se cambió a «4 pasos como máximo» y se enlazó con RNF-01 (menos de 2 minutos). | Andrea (RP) | Sí |
| 2 | RF-09 | Solo impedía cruces del médico; dos médicos podían quedar en el mismo consultorio a la misma hora. Tampoco mencionaba reservas simultáneas. | Se agregó el control por consultorio y el caso de dos usuarios reservando a la vez (riesgo R2 del plan). | Matías (LT) | Sí |
| 3 | RF-12 | No decía cuándo se envía el recordatorio ni cuánto pueden tardar las notificaciones. | Recordatorio entre 24 y 23 h antes; confirmación, reprogramación y cancelación en menos de 5 minutos. | Andrea (RP) | Sí |
| 4 | RNF-04 | Decía «contraseñas seguras» sin indicar cómo. | bcrypt con costo 10 o más, vencimiento de sesión a los 30 minutos y bloqueo tras 5 intentos fallidos. | Matías (LT) | Sí |
| 5 | RF-06 | No decía qué pasa con los turnos ya reservados cuando el médico registra una ausencia. | El sistema lista los turnos afectados y avisa a recepción para reprogramarlos. | Zaith (GP) | Sí |
| 6 | RF-02 | El enlace de recuperación de contraseña no tenía vencimiento. | Vence a los 30 minutos y es de un solo uso. | Matías (LT) | Sí |
| 7 | RF-17 | Incluía «exportar a Excel», que no está en el alcance acordado (2.5). | Se retiró; el reporte se muestra en pantalla. Si el CL lo quiere, se tramita como solicitud de cambio. | Zaith (GP) | Sí |

**Esfuerzo de corrección:** 8 horas-persona de Alexander, registradas como retrabajo de IS.2 en el registro de estado del progreso ([Medición del retrabajo](../06-retrabajo-cierre/medicion-retrabajo.md)).

## Conclusión

El equipo da por **verificada** la Especificación de requisitos en su versión 0.2. Los nueve puntos de la lista se cumplen y las siete observaciones quedaron corregidas. El GP envía la especificación y los prototipos al CL con 48 horas de anticipación, como se acordó en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md), para la validación (IS.2.4).

**Firmas del equipo:**

| Integrante | Firma |
| ------ | ------ |
| Zaith Manangón | ________________ |
| Matías Lugmaña | ________________ |
| Alexander Villacres | ________________ |
| Andrea Raura | ________________ |
