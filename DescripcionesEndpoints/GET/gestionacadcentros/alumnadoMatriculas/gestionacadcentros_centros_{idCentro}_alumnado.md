# Descripción general.

Este endpoint proporciona los datos personales de todo el alumnado de un centro a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 561EBA4551E54E3FBA6BC4CBB8363079)
* **tieneMatriculaCentro**: permite seleccionar al alumnado que está matriculado.
  * No establecido: Devuelve todo el alumnado.
  * Sí: Devuelve al alumnado con matrícula en el centro.
  * No: Devuelve al alumnado que no tiene matrícula en el centro.
* **tieneMatriculaEnCurso**: selecciona al alumnado que está matriculado en el curso escolar indicado (Ej. 2023). Cuando se indica, no es posible elegir la opción "No" del parámetro _tieneMatriculaCentro_.

# Ejemplos.
### A) Solicitud de datos reducidos de todo el alumnado con matrícula en un centro para un idCentro concreto.
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/alumnado?tieneMatriculaCentro=true
   
### B) Solicitud de datos extendidos del alumnado con matrícula en el curso 2023 para un idCentro concreto.
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/alumnado?tieneMatriculaCentro=true & tieneMatriculaEnCurso=2023 & nivelDetalle=e
