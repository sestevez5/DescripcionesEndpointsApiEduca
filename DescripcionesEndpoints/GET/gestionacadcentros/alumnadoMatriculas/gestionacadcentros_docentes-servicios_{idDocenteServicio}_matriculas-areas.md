
# Descripción general.

Este endpoint devuelve la relación de matrículas-áreas vinculadas a un nombramiento docente, es decir, las materias impartidas por un docente a su alumnado, a partir del parámetro _idDocenteServicio_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **fechaReferencia**: Si no se indica, se considerará la fecha actual del sistema. 
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

**Observaciones**: Si el nombramiento no se encontrase vigente en la fechaReferencia, el campo matriculasAreas se devolverá vacío.

## Parámetros específicos.

* **idDocenteServicio**: Obligatorio (Ej. bf51a3a7dbae431ba9fea4cf48cc7c00).

# Ejemplos.

### A) Solicitud de datos con nivelDetalle *reducido* a fecha del sistema de todas las matriculas-áreas asociadas al docente con idDocenteServicio = "06E16894D96A4615A69C000CA34D1D88".
* /gestionacadcentros/docentes-servicios/43BF687B495A44CDAE7372238901943F/matriculas-areas

### B) Solicitud de datos con nivelDetalle *medio* de todas las matriculas-áreas asociadas al docente con idDocenteServicio = "06E16894D96A4615A69C000CA34D1D88" a fecha 05/10/2023.

* /gestionacadcentros/docentes-servicios/43BF687B495A44CDAE7372238901943F/matriculas-areas?fechaReferencia=2023-10-05 & nivelDetalle=m