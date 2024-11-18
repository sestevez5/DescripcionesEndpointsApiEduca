# Descripción general.

Este endpoint proporciona información detallada de las solicitudes del servicio complementario de transporte escolar para una matrícula concreta a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *medio* de las solicitudes de transporte escolar de la matrícula con idMatricula = "9316085667CB4F249BDD220A71A8B045".
* /gestionacadcentros/matriculas/9316085667CB4F249BDD220A71A8B045/servicios-transporte-escolar?nivelDetalle=m