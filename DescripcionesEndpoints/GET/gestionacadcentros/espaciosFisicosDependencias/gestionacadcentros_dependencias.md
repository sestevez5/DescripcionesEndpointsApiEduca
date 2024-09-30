# Descripción general.

Un centro educativo puede estar conformado por uno o varios edificios, cada uno de los cuales puede contener diferentes espacios físicos, que a su vez estarán constituidos por diferentes _dependencias_. Por ejemplo, un edificio puede estar formado por varias plantas, en cada una de las cuales habrá distintas dependencias, como aulas, departamentos, talleres, laboratorios, etc.

Este endpoint devuelve las _dependencias_ de un centro educativo a partir de los parámetros *codigoCentro* y *cursoEscolar*.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), los campos *codigoCentro* y *cursoEscolar* son obligatorios.

## Parámetros comunes.

* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38000263).
* **cursoEscolar**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud con nivelDetalle "medio" de las dependencias del centro con codigoCentro "35010488" para el cursoEscolar = "2022".
* /gestionacadcentros/dependencias?codigoCentro=35010488 & cursoEscolar=2022 & nivelDetalle=m
