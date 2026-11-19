# Verificación del Plan del proyecto — GP.1.13

**Proyecto:** TurnoSalud · **Grupo 6**
**Plan revisado:** [Plan del proyecto](plan-proyecto.md), versión 1.0
**Fecha:** 2026-11-19 · **Registro:** [Acta 03](../actas/ACTA-03_2026-11-19_verificacion-plan.md)
**Resultado:** Plan verificado

---

## Participantes

| Integrante          | Rol     | Qué revisó con más detalle |
|---------------------|---------|----------------------------|
| Zaith Manangón      | GP      | Cálculos PERT (3.5), suma de horas por proceso e integrante (3.6), capacidad (3.7), costo por rol, servicios, reserva y presupuesto total (3.10 a 3.13); coherencia de las cifras entre secciones y tope de USD 18 000. |
| Matías Lugmaña      | LT, PR  | Coherencia del objetivo, alcance, criterios de aceptación y entregables (E1 a E5) frente al Enunciado del trabajo revisado (GP.1.1 y GP.1.2); descomposición técnica de diseño y construcción (IS.3, IS.4), recursos y herramientas tecnológicas (GP.1.5), riesgos técnicos (GP.1.9) y estrategia de control de versiones y uso del repositorio GitHub (GP.1.10 y GP.1.15). |
| Alexander Villacres | AN, DIS | Tareas y productos de IS.2 e IS.3 (3.3), horas asignadas al análisis, al diseño y a la construcción de vistas (3.6), y orden de los procesos en el calendario (3.8). |
| Andrea Raura        | RP, PR  | Tareas de revisión, verificación y validación en cada proceso (3.3), horas de IS.5 y carga semanal de S8 a S10 (3.6 y 3.7), hitos y forma de comprobarlos (3.8), y riesgos relacionados con pruebas (3.14). |

## Puntos revisados

- [x] El objetivo, el alcance y los entregables coinciden con el enunciado revisado.
- [x] Todos los procesos tienen tareas y al menos una revisión o prueba.
- [x] Los cálculos PERT están bien hechos.
- [x] Las horas por integrante no superan la capacidad.
- [x] El calendario cabe en 12 semanas y respeta el orden de los procesos.
- [x] El presupuesto total no pasa de USD 18 000.
- [x] Cada riesgo tiene una respuesta y un responsable.
- [x] El repositorio se usa como dice el plan.

**Comprobaciones numéricas (Zaith):**

- PERT: las ocho filas de 3.5 dan 54 + 20 + 126 + 150 + 438 + 202 + 50 + 108 = **1 148 h-persona**.
- Cada fila de 3.6 suma lo mismo que su fila en 3.5, y los totales por integrante dan 176 + 352 + 319 + 301 = **1 148**.
- Horas por rol en 3.10: 176 + 192 + 319 + 284 + 177 = **1 148**, igual que 3.5.
- Presupuesto: 14 227 + 547 + 2 270 = **USD 17 044**, por debajo de USD 18 000 (margen USD 956).
- Carga semanal máxima: 38 h (Andrea, S8 a S10), por debajo de las 40 h supuestas.

## Observaciones
| Sección del plan | Observación | Corrección | Responsable | ¿Corregido? |
| ------ | ------ | ------ | ------ | ------ |
| 3.1, 3.3 y 3.8 (Alineación con el Enunciado revisado) | Verificar que el objetivo, el alcance incluido/excluido y los 5 entregables con sus semanas de entrega (E1 en S2, E2 en S3, E3 en S5, E4 en S10 y E5 en S12 definidos en la sección 2.6 del Enunciado) coincidan exactamente con los productos de trabajo y los hitos del calendario del Plan. | Se vincularon los entregables E1 a E5 y sus instrucciones de entrega (GP.1.2) con las salidas de los procesos GP e IS y con la tabla de hitos del calendario. | Matías Lugmaña (LT) | Sí |
| 3.9, 3.14 y 3.15 (Recursos técnicos, riesgos y repositorio) | Asegurar que los supuestos técnicos del Enunciado revisado (arquitectura web cliente-servidor, base de datos relacional, alojamiento en la nube y servicio SMTP) y las reglas de trabajo en el repositorio `turno_salud` estén reflejados en el Plan. | Se detallaron los recursos tecnológicos necesarios, el riesgo técnico de cruce de horarios/concurrencia con su plan de mitigación y las convenciones de ramas, commits y versionado en GitHub. Los supuestos técnicos se dejaron por escrito en la sección 2.9 del Enunciado, que la tabla de observaciones citaba pero no existía. | Matías Lugmaña (LT, PR) | Sí |
| 3.10 (Costo por rol) | No quedaba claro cómo se separan las horas de Matías y Andrea entre PR y sus roles de LT y RP, que tienen tarifas distintas. | Se añadió el ejemplo desarrollado de PR: las horas de IS.4 se pagan como PR y el resto como LT o RP. | Zaith Manangón (GP) | Sí |
| 3.6 (Distribución por integrante) | Las 154 h de Alexander en IS.4 podían leerse como trabajo de programador, aunque su rol es AN/DIS. | Se aclaró debajo de la tabla que corresponden a construir las vistas que él mismo diseñó y que se cobran con la tarifa de AN/DIS. | Alexander Villacres (AN, DIS) | Sí |
| 3.7 (Capacidad) | Con solo la utilización global (59,8 %) no se veían los picos de carga de S8 a S10, cuando las pruebas coinciden con el final de la construcción. | Se agregó la tabla de carga semanal por integrante y el comentario de las semanas más cargadas, con quién puede apoyar si hay retraso. | Andrea Raura (RP, PR) | Sí |

## Conclusión

El equipo revisó el Plan del proyecto versión 1.0 y lo da por **verificado**. Los ocho puntos se cumplen, las cifras coinciden entre secciones y las cinco observaciones quedaron corregidas antes del cierre de la reunión. El plan puede presentarse al cliente para su revisión y aceptación (GP.1.14), lo que se registra en el [Acta 04](../actas/ACTA-04_2026-11-20_aceptacion-plan-cliente.md).

**Firmas del equipo:**
| Integrante | Firma |
| ------ | ------ |
| Zaith Manangón | ________________ |
| Matías Lugmaña | ________________ |
| Alexander Villacres | ________________ |
| Andrea Raura | ________________ |
