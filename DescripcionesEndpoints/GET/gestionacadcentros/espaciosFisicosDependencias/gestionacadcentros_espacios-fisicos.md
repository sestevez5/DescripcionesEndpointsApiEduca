# Descripción general.

Este endpoint devuelve los espacios físicos de un centro educativo (Aulas, salas, talleres, etc.) a partir del parámetro *codigoCentro*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *codigoCentro* es obligatorio.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38000263).

# Ejemplos.
### A) Solicitud de los espacios físicos del centro con codigoCentro "35010488".
* ?codigoCentro=35010488
