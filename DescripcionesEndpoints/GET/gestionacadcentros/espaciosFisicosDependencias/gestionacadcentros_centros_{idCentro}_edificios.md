# Descripción general.

Este endpoint proporciona los diferentes edificios que conforman un centro educativo a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *idCentro* es obligatorio.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 33283FBB-18B1-4195-93B1-179785FAC806)

# Ejemplo.
### A) Solicitud de datos de los edificios del centro con idCentro "C372B7FE-132A-4806-BA55-B6BD259F33D6".
* C372B7FE-132A-4806-BA55-B6BD259F33D6/edificios
