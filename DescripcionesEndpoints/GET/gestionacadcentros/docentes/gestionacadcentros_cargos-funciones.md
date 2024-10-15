# Descripción general.

Este endpoint devuelve información relativa a los cargos y funciones (dirección, jefatura de estudios, coordinaciones, jefaturas de departamento, etc.) de un centro educativo a partir de su _codigoCentro_.

## Parámetros comunes.
* **codigoCentro**: Obligatorio (Ej. 38010773)
* **cursoEscolar**: Obligatorio (Ej. 2021)
* **esCargoDirectivo**: Si se selecciona "Sí", solo se muestran los cargos directivos.
* **fechaReferencia**: Si no se especifica, se mostrarán todos los cargos y funciones para el curso escolar indicado.
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *medio* de todos los cargos y funciones del centro con código "35010488" en el curso 2023 a partir del 10/01/2024.
* /gestionacadcentros/cargos-funciones?codigoCentro=35010488 & cursoEscolar=2023 & fechaReferencia=2024-01-10 & nivelDetalle=m

### B) Solicitud de datos con nivelDetalle *reducido* de los cargos directivos del centro con código "35010488" en el curso 2024.
* /gestionacadcentros/cargos-funciones?codigoCentro=35010488 & cursoEscolar=2024 & esCargoDirectivo=true

### C) Solicitud de datos con nivelDetalle *reducido* de los cargos y funciones *no directivas* del centro con código "35010488" en el curso 2022.
* /gestionacadcentros/cargos-funciones?codigoCentro=35010488 & cursoEscolar=2022 & esCargoDirectivo=false & nivelDetalle=r
