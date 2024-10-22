
# Descripción general.

Este endpoint devuelve las matrículas asociadas a un nombramiento docente, es decir, el alumnado de un docente a partir del parámetro _idDocenteServicio_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idDocenteServicio**: Obligatorio (Ej. bf51a3a7dbae431ba9fea4cf48cc7c00).

# Ejemplos.

### A) Solicitud de todos las matriculas asociadas al docente con idDocenteServicio = "06E16894D96A4615A69C000CA34D1D88".
* /gestionacadcentros/docentes-servicios/06E16894D96A4615A69C000CA34D1D88/matriculas

