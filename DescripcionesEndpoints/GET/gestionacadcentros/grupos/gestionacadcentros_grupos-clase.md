# Descripción general.

Este endpoint devuelve información de los grupos clase de un centro educativo.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

**Observaciones**:
* Opción 1: Los campos obligatorios son el *cursoEscolar* y el *codigoCentro*.
* Opción 2: El campo *idCursoCentro* es obligatorio.

## Parámetros específicos.

### Opción 1.
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773).
* **idEstudioSC**: Optativo. No se puede especificar simultáneamente con el campo *idEnsenyanzaSC* (Ej. 232)
* **idEnsenyanzaSC**: Optativo. No se puede especificar simultáneamente con el campo *idEstudioSC* (Ej. 26)

**Observaciones**: Los campos *idCursoCentro*, *IdEstudio*, *IdEnsenyanza* no están permitidos en esta opción.

### Opción 2.
* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idEstudio**: Optativo. No se puede especificar simultáneamente con el campo *idEnsenyanza* (Ej. FB122AE637F445AFBED5F401C0AB6E87)
* **idEnsenyanza**: Optativo. No se puede especificar simultáneamente con el campo *idEstudio* (Ej. 5FF2F0FD02AD44F08D39EF37774F9569)

**Observaciones**: Los campos *cursoEscolar*, *codigoCentro*, *idEstudioSC*, *idEnsenyanzaSC* no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todos los grupos clase con nivelDetalle *medio* del centro con código = "38011327" en el curso 2022.
* /gestionacadcentros/grupos-clase?opcion=1 & cursoEscolar=2022 & codigoCentro=38011327 & nivelDetalle=m

### B) Solicitud de los grupos clase con nivelDetalle *reducido* de una enseñanza concreta del centro con código = "35007374" en el curso 2021.
* /gestionacadcentros/grupos-clase?opcion=1 & cursoEscolar=2021 & codigoCentro=38011327 & idEnsenyanzaSC=9

### C) Solicitud de todos los grupos clase con nivelDetalle *medio* para el idCursoCentro = "D2F5FE18A3124939B8CC46D8E8EF46FF".
* /gestionacadcentros/grupos-clase?opcion=2 & idCursoCentro=D2F5FE18A3124939B8CC46D8E8EF46FF & nivelDetalle=m

### D) Solicitud de los grupos clase con nivelDetalle *reducido* del estudio con idEstudio = "89FC278E0BFF419081972F18A0C07516" e idCursoCentro = "D2F5FE18A3124939B8CC46D8E8EF46FF" .
* /gestionacadcentros/grupos-clase?opcion=2 & idCursoCentro=D2F5FE18A3124939B8CC46D8E8EF46FF & idEstudio=89FC278E0BFF419081972F18A0C07516
