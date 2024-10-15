# Descripción general.

Este endpoint proporciona los diferentes espacios físicos (Aulas, salas, talleres, etc.) que conforman un centro educativo a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *idCentro* es obligatorio.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 33283FBB18B1419593B1179785FAC806)

# Ejemplo.
### A) Solicitud de los espacios físicos del centro con idCentro = "C372B7FE132A4806BA55B6BD259F33D6".
* /gestionacadcentros/centros/C372B7FE132A4806BA55B6BD259F33D6/espacios-fisicos
