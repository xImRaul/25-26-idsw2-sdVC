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
