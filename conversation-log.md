# Conversation Log — Inicio del proyecto Jorgestor

---

## [1:01] Inicio de sesión — Presentación del proyecto y estudio del repositorio

**Prompt:** "tengo que hacer un proyecto para clase en el que tengo que codificar enteramente contido un proyecto que tenemos modelado... el modelado lo tengo todo en un github... quiero trabajar como lo he hecho en el repo de modelado... quiero que te estudies este repositorio https://github.com/martinlopez7/25-26-IdSw1-SdR"

**Resultado:** Se leyeron las páginas principales del repositorio de GitHub:
- `README.md` raíz → descripción general del sistema Jorgestor
- `documents/modelos/diagramas/README.md` → inventario de diagramas de entidades, objetos y estados
- `documents/casos-de-uso/encontrarActoresYCasosDeUso/README.md` → actores: Docente, Administrador Institucional, Tiempo
- `documents/casos-de-uso/detalladoCasosDeUso/README.md` → listado completo de ~30 casos de uso detallados

Resumen producido:
- **Sistema:** Jorgestor — generación, asignación y corrección automática (con IA) de exámenes personalizados para docentes universitarios.
- **Actores:** Docente (principal), Administrador Institucional, Tiempo (cierre de sesión por inactividad).
- **Entidades del dominio:** Docente, AdministradorInstitucional, Alumno, Grado, Asignatura, Pregunta, Respuesta, Examen.
- **Casos de uso:** autenticación, CRUD completo de todas las entidades, generación/asignación/corrección de exámenes, importación/exportación de datos.
- **Estructura del repo:** `documents/modelos/`, `documents/casos-de-uso/` con subcarpetas por disciplina, cada caso de uso con `.puml` + `.svg`.

**Decisión:** Aceptado íntegramente. El AI capturó correctamente la arquitectura del modelado y la estructura de carpetas. Se solicitó al usuario que aclarase stack tecnológico, punto de partida (casos priorizados vs. arquitectura base) y si trabaja en equipo o en solitario, para poder orientar la codificación de forma ordenada.

## [1:35] Evaluación del stack 

**Prompt:** "Dime un stack inicial para empezar este proyecto para que sea lo mas cohesivo, eficiente y lo mas óptimo para el trabajo"

**Resultado:** El AI produjo una tabla de evaluación comparativa con los siguientes criterios por capa:

*Backend (NestJS vs Spring Boot vs FastAPI):*
- Alineación con el modelado OO: NestJS alta (módulos = casos de uso), Spring Boot alta pero Java, FastAPI media.
- Curva de aprendizaje en solitario: NestJS media (TypeScript conocido), Spring Boot alta, FastAPI baja.
- Estructura modular explícita: NestJS sí (decoradores + DI nativo), FastAPI no (manual).
- Guards / Auth JWT: NestJS integrado (`AuthGuard`), Spring Boot requiere Spring Security, FastAPI manual.
- Viabilidad proyecto individual: NestJS y FastAPI altas, Spring Boot media por ser verboso.

*Frontend (Angular vs React vs Vue):*
- Coherencia con NestJS: Angular muy alta (TypeScript nativo compartido), React y Vue altas.
- Estructura por módulos/features: Angular impuesta por framework, React manual, Vue semi-impuesta.
- Curva de aprendizaje en solitario: Angular alta (muchos conceptos simultáneos), React media, Vue baja-media.
- Formularios complejos (generación de exámenes): Angular muy bueno con Reactive Forms.

*Base de datos (PostgreSQL + Prisma):*
- PostgreSQL encaja con el modelo relacional: FK entre Examen, Pregunta, Alumno, Asignatura.
- Prisma genera tipos TypeScript automáticamente desde el schema → tipado extremo a extremo.
- `prisma migrate` genera migraciones automáticas: una sola fuente de verdad.
- Viabilidad individual alta: Prisma elimina SQL manual.

Veredicto del AI: **stack sólido y coherente**, con un riesgo identificado: Angular tiene la curva de aprendizaje más alta de los tres frontends para un desarrollador en solitario (módulos, servicios inyectables, Reactive Forms, Guards, interceptores HTTP simultáneamente). Recomendación: acotar desde ya qué casos de uso se implementan completamente en Angular, usando la priorización del modelado como guía.

**Decisión:** Stack aceptado: **NestJS + Angular + PostgreSQL + Prisma**. Se nota el riesgo de Angular como punto a vigilar. Se retoma el diseño paso a paso ya con NestJS en mente en lugar de Express.

---

> **Nota:** Este log no se reescribe. Las siguientes entradas se añadirán cronológicamente a medida que avance el proyecto.
