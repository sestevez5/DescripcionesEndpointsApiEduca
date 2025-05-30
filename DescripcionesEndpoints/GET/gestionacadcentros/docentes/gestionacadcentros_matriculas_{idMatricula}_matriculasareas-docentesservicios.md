
# Descripción general.

Este endpoint devuelve una colección de áreas matrículas y sus correspondientes docentes servicios a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.
Es decir, para un alumnado concreto proporciona las materias en las que está matriculado y los docentes que las imparten.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **fechaReferencia**: Devuelve solo los servicios docentes que formen parte de la plantilla funcional en esta fecha (Ej. 2024-11-29). Si no se indica, se usará la fecha del sistema.
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *medio* de las áreas matrículas y sus correspondientes docentes servicios de la matrícula con idMatricula = "FBDB045262C84349A7EC2FB5E00766B3" a fecha del sistema.
* /gestionacadcentros/matriculas/FBDB045262C84349A7EC2FB5E00766B3/matriculasareas-docentesservicios?nivelDetalle=m

