
# Descripción general.

Este endpoint devuelve información de los resultados de todas las matrículas-áreas (asignaturas) en una evaluación concreta para todas las matrículas (alumnado) de un grupo clase determinado a partir del parámetro *idGrupo*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idSesionEvaluacion**: Obligatorio (Ej. 9EB0219DBB1D4AA6BE66DDAE9DDDE577).
* **idArea**: Si se indica, solo devolverá información de la evaluación las matrículas-áreas correspondientes al área especificada, es decir, los resultados obtenidos por el alumnado de una determinada materia (Ej. 977b2e3c9eff4dbbb71f0ac4f6554699).
* **idDocenteServicio**: Si se indica, solo devolverá información de los resultados de la evaluación de las matrículas-áreas impartidas por el docente al grupo clase en la sesión de evaluación especificada, es decir, los resultados de las materias impartidas por el docente (Ej. E3363F92B2AF478CAAF25B5BA1BF50FA).
* **idGrupo**: Obligatorio (Ej. A2E61D953ECA49A283FB456D144800E8).

# Ejemplos.
### A) Solicitud de datos de los resultados obtenidos por el grupo con idGrupo = "A2E61D953ECA49A283FB456D144800E8" en la sesión de evaluación con idSesionEvaluacion = "9EB0219DBB1D4AA6BE66DDAE9DDDE577" .
* /gestionacadcentros/grupos/A2E61D953ECA49A283FB456D144800E8/resultado-evaluacion-matriculasareas?idSesionEvaluacion=9EB0219DBB1D4AA6BE66DDAE9DDDE577

### B) Solicitud de datos de los resultados del área con idArea = "977b2e3c9eff4dbbb71f0ac4f6554699" obtenidos por el grupo con idGrupo = "A2E61D953ECA49A283FB456D144800E8" en la sesión de evaluación con idSesionEvaluacion = "9EB0219DBB1D4AA6BE66DDAE9DDDE577" .
* /gestionacadcentros/grupos/A2E61D953ECA49A283FB456D144800E8/resultado-evaluacion-matriculasareas?idSesionEvaluacion=9EB0219DBB1D4AA6BE66DDAE9DDDE577 & idArea=977b2e3c9eff4dbbb71f0ac4f6554699

### C) Solicitud de datos de los resultados del área con idArea = "5c5558414b134410acad09d4bf75eb3f" impartida por el docente con idDocenteServicio = "184BE527232B42839B034AB629A40B6F" obtenidos por el grupo con idGrupo = "AEF562823308464B8E5D1CE37B44AD37" en la sesión de evaluación con idSesionEvaluacion = "9785A9DA764E4BEEB4AD86CAC6D86EBE" .
* /gestionacadcentros/grupos/AEF562823308464B8E5D1CE37B44AD37/resultado-evaluacion-matriculasareas?idSesionEvaluacion=9785A9DA764E4BEEB4AD86CAC6D86EBE & idArea=5c5558414b134410acad09d4bf75eb3f & idDocenteServicio=184BE527232B42839B034AB629A40B6F

