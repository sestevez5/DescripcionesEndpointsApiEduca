# Descripción general.

Este endpoint devuelve las dependencias de un centro educativo (Espacio físico, edificio, agrupación funcional, código, etc.) a partir de los parámetros *codigoCentro* y *cursoEscolar*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), los campos *codigoCentro* y *cursoEscolar* son obligatorios.

## Parámetros comunes.

* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38000263).
* **cursoEscolar**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud con nivelDetalle "medio" de las dependencias del centro con codigoCentro "35010488" para el cursoEscolar = "2022".
* ?codigoCentro=35010488 & cursoEscolar=2022 & nivelDetalle=m
