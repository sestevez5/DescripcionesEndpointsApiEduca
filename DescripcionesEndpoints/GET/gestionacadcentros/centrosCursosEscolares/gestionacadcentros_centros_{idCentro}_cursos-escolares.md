# Descripción general.

Este endpoint proporciona los cursos escolares de un centro educativo (idCursoCentro, fechaInicio, etc.) a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 3793A6D1C74242EDB005DA3529421EE5)

# Ejemplo.
### A) Solicitud de los cursos escolares del centro con idCentro "561EBA4551E54E3FBA6BC4CBB8363079".
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/cursos-escolares
