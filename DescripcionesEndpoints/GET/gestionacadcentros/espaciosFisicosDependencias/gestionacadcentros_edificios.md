# Descripción general.

Un centro educativo puede estar conformado por uno o varios _edificios_, cada uno de los cuales puede contener diferentes espacios físicos, que a su vez estarán constituidos por diferentes dependencias. Por ejemplo, un edificio puede estar formado por varias plantas, en cada una de las cuales habrá distintas dependencias, como aulas, departamentos, talleres, laboratorios, etc.

Este endpoint devuelve los diferentes _edificios_ que conforman un centro educativo a partir del parámetro *codigoCentro*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *codigoCentro* es obligatorio.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38003306).

# Ejemplos.
### A) Solicitud de los edificios del centro con codigoCentro = "35015887".
* ?codigoCentro=35015887
