# Descripción general.

Un centro educativo puede estar conformado por uno o varios edificios, cada uno de los cuales puede contener diferentes _espacios físicos_, que a su vez estarán constituidos por diferentes dependencias. Por ejemplo, un edificio puede estar formado por varias plantas, en cada una de las cuales habrá distintas dependencias, como aulas, departamentos, talleres, laboratorios, etc.

Este endpoint devuelve los _espacios físicos_ de un centro educativo a partir del parámetro *codigoCentro*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *codigoCentro* es obligatorio.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38000263).

# Ejemplos.
### A) Solicitud de los espacios físicos del centro con codigoCentro "35010488".
* /gestionacadcentros/espacios-fisicos?codigoCentro=35010488
