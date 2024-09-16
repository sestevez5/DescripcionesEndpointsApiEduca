# Descripción general.

Este endpoint devuelve los estudios impartidos en un centro educativo a partir.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo.

**Observaciones**:
* Opción 1: Los campos obligatorios son el cursoEscolar y el codigoCentro.
* Opción 2: El campo idCursoCentro es obligatorio.

## Parámetros específicos.

### Opción 1.
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: El campo idCursoCentro no está permitido en esta opción.

### Opción 2.
* **idCursoCentro**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).

**Observaciones**: Los campos cursoEscolar y codigoCentro no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de los estudios, incluidos los no ofertados, para el idCursoCentro especificado .
* ?opcion=2 & incluirNoOfertados=true & idCursoCentro=0D95CCCE-E390-4190-B1F8-10A90A4B7477

### B) Solicitud de todos los estudios del centro con código "38016519" en el curso 2022.
* ?opcion=1 & cursoEscolar=2022 & codigoCentro=38016519
