# Descripción general.

Este endpoint proporciona información detallada de los resultados obtenidos por una matrícula concreta en una sesión de evaluación determinada a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **idSesionEvaluacion**: Obligatorio (Ej. 52f1c372c1db4f49bd06f551e0989b98)

# Ejemplos.
### A) Solicitud de datos de los resultados obtenidos por la matrícula con idMatricula = "F0624792913E4CBBAA26225B9AC29BFC" en la sesión de evaluación con idSesionEvaluacion = "52f1c372c1db4f49bd06f551e0989b98" .
* /gestionacadcentros/matriculas/F0624792913E4CBBAA26225B9AC29BFC/resultado-evaluacion?idSesionEvaluacion=52f1c372c1db4f49bd06f551e0989b98
