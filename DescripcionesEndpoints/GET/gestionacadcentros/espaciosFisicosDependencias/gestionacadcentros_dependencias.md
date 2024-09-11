# Descripción general.

Este endpoint devuelve las dependencias de un centro educativo (Espacio físico, edificio, etc.) a partir de los parámetros *codigoCentro* y *cursoEscolar*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), los campos *codigoCentro* y *cursoEscolar* son obligatorios.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38000263).
* **cursoEscolar**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud de los espacios físicos del centro con codigoCentro "35010488".
* ?codigoCentro=35010488
