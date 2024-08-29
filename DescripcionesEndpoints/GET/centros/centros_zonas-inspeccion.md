# Descripción general

Este endpoint devuelve los responsables de las diferentes zonas de inspección.

## Parámetros comunes
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

**Observaciones**:


* Opción 1: Los campos obligatorios son el cursoEscolar y el codigoCentro.
* Opción 2: El campo idCursoCentro es obligatorio.

## Parámetros específicos

### Opción 1
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773).
* **idEstudioSC**: Optativo. No se puede especificar simultáneamente con el campo *idEnsenyanzaSC* (Ej. 232)
* **idEnsenyanzaSC**: Optativo. No se puede especificar simultáneamente con el campo *idEstudioSC* (Ej. 26)

**Observaciones**: Los campos idCursoCentro, IdEstudio, IdEnsenyanza no están permitidos en esta opción.
