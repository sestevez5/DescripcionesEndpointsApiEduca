
# Descripción general.

Este endpoint proporciona información detallada de las solicitudes del servicio complementario de ayuda libros y material didáctico para una matrícula concreta a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. D15755D7E45F4E3E9C262EE73FAD46BB)
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *medio* de las solicitudes de ayuda libros y material didáctico de la matrícula con idMatricula = "D15755D7E45F4E3E9C262EE73FAD46BB".
* /gestionacadcentros/matriculas/D15755D7E45F4E3E9C262EE73FAD46BB/servicios-ayudas-libros-material?nivelDetalle=m




