# Descripción general.

Este endpoint devuelve información relativa a las zonas de inspección en materia educativa (responsable, denominación, etc.)) en las que está dividida la Comunidad Educativa.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *cursoEscolar* es obligatorio.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud de las zonas de inspección para el curso "2024".
* ?cursoEscolar=2024

