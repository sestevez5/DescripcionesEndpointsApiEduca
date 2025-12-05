
# Descripción general.

Este endpoint proporciona información detallada de las solicitudes del servicio complementario de desayuno para una matrícula concreta a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *extendido* de las solicitudes de comedor escolar de la matrícula con idMatricula = "D15755D7E45F4E3E9C262EE73FAD46BB".
* /gestionacadcentros/matriculas/D15755D7E45F4E3E9C262EE73FAD46BB/servicios-desayuno?nivelDetalle=e



