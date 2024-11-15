
# Descripción general.

Este endpoint proporciona información detallada de las solicitudes del servicio complementario de comedor escolar para una matrícula concreta a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *extendido* de la solicitud de comedor escolar de la matrícula con idMatricula = "77BFC14B73F14CF7A6A9200285DD19D5".
* /gestionacadcentros/matriculas/77BFC14B73F14CF7A6A9200285DD19D5/servicios-comedor-escolar?nivelDetalle=e




