# 6a. Medición del retrabajo — GP y RP

**Proyecto:** TurnoSalud · **Grupo 6**
**Responsables:** Zaith Manangón (GP) y Andrea Raura (RP) · **Apoyo:** Matías Lugmaña (LT) y Alexander Villacres (AN/DIS)
**Tareas de la norma:** GP.3.1 Evaluar el avance frente al plan · GP.3.2 Establecer acciones correctivas
**Línea base:** [Plan del proyecto v1.1](../03-plan-proyecto/plan-proyecto.md) (sección 3.18)
**Semana del proyecto:** S12 · **Registro:** [Acta 08](../actas/ACTA-08_2026-11-23_cierre-proyecto.md)

> **Datos simulados.** El taller no construye el software. Las horas reales, los defectos y los resultados de S3 a S12 son supuestos del ejercicio, coherentes con el plan, para practicar cómo se mide el retrabajo y se cierra un proyecto.

---

## 6.1 Qué es retrabajo y qué no

**Retrabajo** son las horas que se gastan en rehacer algo que ya se había dado por terminado porque tenía un defecto: corregir un requisito ambiguo, rehacer un diagrama, arreglar código que falló una prueba, corregir un manual.

Para medirlo, cada integrante clasificó sus horas de la semana en cuatro categorías, las mismas del caso BitPerfect visto en clase:

| Categoría | Qué incluye | Ejemplos en TurnoSalud |
|-----------|-------------|------------------------|
| **Ejecución** | Hacer el trabajo por primera vez | Redactar la especificación, programar el agendamiento, implementar SC-01 |
| **Revisión** | Verificar, validar y probar | Verificación del plan y de la especificación, revisión de código, ejecución de pruebas, validación con el CL |
| **Retrabajo** | Corregir defectos encontrados en una revisión o prueba | Las 7 observaciones de la verificación de requisitos, los defectos de concurrencia de RF-09 |
| **Prevención** | Evitar defectos antes de que ocurran | Taller de ISO/IEC 29110, nivelación en NestJS y Prisma, listas de verificación, reglas de linter |

**Lo que no cuenta como retrabajo:**

- **Las horas de la solicitud de cambio SC-01.** Es trabajo nuevo que pidió el cliente después de validar los requisitos, no la corrección de un error del equipo. Se registran como ejecución y revisión.
- **Las horas de revisión y pruebas.** Encuentran los defectos, pero no los corrigen. Son el costo de evaluar la calidad.

Las correcciones que pidió el CL al validar la especificación (V-01 a V-04) **sí** son retrabajo: corrigen requisitos que estaban incompletos.

**Fórmula:**

**% de retrabajo = horas de retrabajo ÷ horas totales reales × 100**

## 6.2 Fuentes de datos

- **Registro de estado del progreso:** en la reunión de cada lunes (Plan 3.16), cada integrante informó sus horas de la semana por proceso y por categoría. El GP las consolidó.
- **Registro de defectos:** cada defecto encontrado en una verificación, validación, revisión de código o prueba se anotó con la actividad que lo detectó y las horas que tomó corregirlo. Lo mantiene Andrea (RP).

## 6.3 Esfuerzo real frente al plan (GP.3.1)

| Proceso | Plan v1.1 (h) | Real (h) | Desviación (h) | Desviación (%) |
|---------|---------------|----------|----------------|----------------|
| GP.1 Planificación | 54 | 56 | +2 | +3,7 % |
| IS.1 Inicio de la implementación | 20 | 20 | 0 | 0,0 % |
| IS.2 Análisis de requisitos | 134 | 140 | +6 | +4,5 % |
| IS.3 Arquitectura y diseño detallado | 158 | 162 | +4 | +2,5 % |
| IS.4 Construcción | 462 | 488 | +26 | +5,6 % |
| IS.5 Integración y pruebas | 210 | 222 | +12 | +5,7 % |
| IS.6 Entrega del producto | 52 | 52 | 0 | 0,0 % |
| GP.2 a GP.4 Seguimiento y cierre | 112 | 114 | +2 | +1,8 % |
| **Total** | **1 202** | **1 254** | **+52** | **+4,3 %** |

| Integrante | Plan v1.1 (h) | Real (h) | Desviación (h) |
|------------|---------------|----------|----------------|
| Zaith      | 181 | 184 | +3 |
| Matías     | 373 | 392 | +19 |
| Alexander  | 331 | 340 | +9 |
| Andrea     | 317 | 338 | +21 |
| **Total**  | **1 202** | **1 254** | **+52** |

Ningún proceso cerró por encima del umbral de 10 % del plan (3.16), pero IS.4 sí lo pasó a mitad de camino (sección 6.7).

## 6.4 Horas reales por categoría

| Proceso | Ejecución | Revisión | Retrabajo | Prevención | Total | % retrabajo |
|---------|-----------|----------|-----------|------------|-------|-------------|
| GP.1 Planificación | 34 | 8 | 6 | 8 | 56 | 10,7 % |
| IS.1 Inicio de la implementación | 10 | 2 | 0 | 8 | 20 | 0,0 % |
| IS.2 Análisis de requisitos | 96 | 22 | 18 | 4 | 140 | 12,9 % |
| IS.3 Arquitectura y diseño detallado | 118 | 20 | 16 | 8 | 162 | 9,9 % |
| IS.4 Construcción | 360 | 48 | 72 | 8 | 488 | 14,8 % |
| IS.5 Integración y pruebas | 40 | 120 | 62 | 0 | 222 | 27,9 % |
| IS.6 Entrega del producto | 40 | 6 | 4 | 2 | 52 | 7,7 % |
| GP.2 a GP.4 Seguimiento y cierre | 98 | 12 | 4 | 0 | 114 | 3,5 % |
| **Total** | **796** | **238** | **182** | **38** | **1 254** | **14,5 %** |
| **% del total** | 63,5 % | 19,0 % | **14,5 %** | 3,0 % | 100 % | |

El 27,9 % de IS.5 no significa que las pruebas se hicieron mal: ahí se corrigen los defectos que las pruebas encuentran en el código. Por eso conviene leer el retrabajo por la actividad que detectó el defecto (6.6).

## 6.5 Resultado

**% de retrabajo = 182 ÷ 1 254 × 100 = 14,5 %**

**Costo del retrabajo ≈ 182 h × USD 12,35/h = USD 2 247**, donde USD 12,35/h es la tarifa promedio real del proyecto (USD 15 482 de trabajo ÷ 1 254 h).

**Comparación con las referencias de clase:**

| Proyecto | Ejecución | Revisión | Retrabajo | Prevención |
|----------|-----------|----------|-----------|------------|
| TurnoSalud (1 254 h) | 63,5 % | 19,0 % | **14,5 %** | 3,0 % |
| BitPerfect, Perú (882 h; García, 2015) | 66,3 % | 14,1 % | **18,0 %** | 1,6 % |
| Sin proceso definido (Charette, 2005) | — | — | **40 a 50 %** | — |

TurnoSalud dedicó más horas a revisar (19,0 % frente a 14,1 %) y a prevenir (3,0 % frente a 1,6 %) que BitPerfect, y tuvo menos retrabajo (14,5 % frente a 18,0 %). Juntas, revisión y prevención suman 276 h (22,0 %): es la inversión en calidad que hace que el retrabajo quede muy por debajo del 40 a 50 % que reporta Charette.

## 6.6 Defectos y retrabajo por actividad de detección

| Actividad que detectó el defecto | Semana | Defectos | Horas de corrección | Horas por defecto |
|----------------------------------|--------|----------|---------------------|-------------------|
| Verificación del plan (GP.1.13) | S2 | 5 | 6 | 1,2 |
| Verificación de la especificación (IS.2.3) | S3 | 7 | 8 | 1,1 |
| Validación de la especificación con el CL (IS.2.4) | S3 | 4 | 10 | 2,5 |
| Verificación del diseño (IS.3) | S5 | 6 | 16 | 2,7 |
| Revisión de código y pruebas unitarias (IS.4) | S5 a S10 | 28 | 72 | 2,6 |
| Pruebas de integración y de sistema (IS.5) | S8 a S11 | 15 | 50 | 3,3 |
| Validación del sistema con el CL (IS.5) | S11 | 3 | 12 | 4,0 |
| Verificación de la entrega (IS.6) | S12 | 1 | 4 | 4,0 |
| Revisión de informes y actas (GP.2 a GP.4) | S3 a S12 | 2 | 4 | 2,0 |
| **Total** | | **71** | **182** | **2,6** |

Además quedaron 2 defectos menores abiertos al cierre, aceptados por el CL ([Informe de cierre](informe-cierre.md)).

**Lo que muestran los datos:**

1. **Un defecto cuesta más cuanto más tarde se encuentra.** Los 22 defectos encontrados en el plan, los requisitos y el diseño costaron 1,8 h cada uno (40 h en total). Los 19 encontrados en pruebas de sistema, validación final y entrega costaron 3,5 h cada uno (66 h). Casi el doble.
2. **El retrabajo se concentra en construcción y pruebas:** IS.4 e IS.5 suman 134 de las 182 h (73,6 %).
3. **El riesgo R2 apareció en pruebas.** Dos de los 15 defectos de IS.5 fueron turnos cruzados en el mismo consultorio con reservas simultáneas: la restricción única de la base de datos cubría médico, fecha y hora, pero no el consultorio. Se corrigieron en 14 h. La observación 2 de la verificación de requisitos ya había pedido controlar el consultorio, pero no llegó completa al diseño.
4. **La validación temprana con el CL funcionó.** Las 4 observaciones de la validación de requisitos (2,5 h cada una) habrían costado más si aparecían recién en la validación del sistema (4,0 h cada una).

## 6.7 Acción correctiva AC-01 (GP.3.2)

| Campo | Valor |
|-------|-------|
| **Semana** | S8 |
| **Problema** | En la evaluación del lunes, IS.4 iba 11 % por encima de las horas planificadas a esa fecha: pasó el umbral de 10 % (Plan 3.16). Causas: los defectos de concurrencia del agendamiento y el ajuste de la cancelación por SC-01. Andrea iba a llegar a 42 h en S9. |
| **Acciones** | 1) Alexander toma 8 h de pantallas de recepción en S10, como prevé el plan (3.7). 2) Las pruebas de concurrencia (CP-09) se adelantan a S8 y la transacción de reserva pasa por revisión de código en pareja (Matías y Andrea). 3) El GP revisa las horas de IS.4 dos veces por semana hasta S10. |
| **Responsables** | Zaith (GP) y Matías (LT) |
| **Costo** | Sin costo adicional: se reasignan horas dentro del equipo. |
| **Resultado** | IS.4 cerró en +5,6 % y la versión beta (E4) se entregó en S10, a tiempo. El primer incremento en staging se atrasó de S7 a S8, una semana, dentro del umbral. |
| **Estado** | Cerrada en S10 |

## 6.8 Conclusiones y recomendaciones

- **Resultado:** 14,5 % de retrabajo, por debajo del 18 % de BitPerfect y muy lejos del 40 a 50 % de referencia. La desviación total de esfuerzo fue de +4,3 %.
- **Para el próximo proyecto:** fijar en el plan una meta de retrabajo de 12 % como máximo y medirla desde la semana 1.
- **Pruebas de concurrencia desde el diseño:** incluir en la lista de verificación del diseño una pregunta por cada regla de «no cruce» (médico, consultorio, paciente) y escribir CP-09 antes de construir el agendamiento.
- **Trazabilidad requisito → diseño:** revisar que cada observación de la verificación de requisitos llegue al diseño, para que no se repita lo del consultorio.
- **Clasificar horas desde el primer día:** el registro por categorías es lo que permitió medir el retrabajo; debe ser parte de la plantilla del registro de estado del progreso.
