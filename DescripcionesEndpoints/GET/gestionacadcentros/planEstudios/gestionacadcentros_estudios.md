# Descripción general.

Este endpoint devuelve los estudios impartidos en los centros educativos (Ej. *2º Educación Secundaria Obligatoria (LOMLOE)*, *1º CFGS Sanidad - Dietética*, etc.).

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo. Si se escoge "No" o "No establecido", devuelve solo los estudios ofertados.

**Observaciones**:
* Opción 1: Los campos obligatorios son el cursoEscolar y el codigoCentro.
* Opción 2: El campo idCursoCentro es obligatorio.

## Parámetros específicos.

### Opción 1.
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773).

**Observaciones**: El campo idCursoCentro no está permitido en esta opción.

### Opción 2.
* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).

**Observaciones**: Los campos cursoEscolar y codigoCentro no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de los estudios, incluidos los no ofertados, para el idCursoCentro especificado .
* /gestionacadcentros/estudios?opcion=2 & incluirNoOfertados=true & idCursoCentro=0D95CCCEE3904190B1F810A90A4B7477

### B) Solicitud de todos los estudios del centro con código "38016519" en el curso 2022.
* /gestionacadcentros/estudios?opcion=1 & cursoEscolar=2022 & codigoCentro=38016519

