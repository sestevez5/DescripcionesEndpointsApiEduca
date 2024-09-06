# Descripción general.

Este endpoint devuelve los diferentes edificios que conforman un centro educativo a partir del parámetro *codigoCentro*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *codigoCentro* es obligatorio.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38003306).

# Ejemplos.
### A) Solicitud de los edificios del centro con codigoCentro = "35015887".
* ?codigoCentro=35015887
