# Descripción general

Este endpoint proporciona los datos personales de todo el alumnado de un centro a partir del parámetro *idCentro*.

## Parámetros comunes
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

## Parámetros específicos

* **idCentro**: Obligatorio (Ej. 561EBA45-51E5-4E3F-BA6B-C4CBB8363079)
* **tieneMatriculaCentro**: permite seleccionar al alumnado que está matriculado.
  * No establecido: Devuelve todo el alumnado.
  * 
* **tieneMatriculaEnCurso**: selecciona al alumnado que está matriculado en el curso escolar indicado (Ej. 2023).

# Ejemplos.
### A) Solicitud de datos del alumno para el idAlumnoCentro = "ba9b30a2-2d88-4b60-ba19-000c86f9e462".
* ba9b30a2-2d88-4b60-ba19-000c86f9e462
