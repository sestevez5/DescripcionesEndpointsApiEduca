
# Descripción general.

Este endpoint proporciona las fotos del personal docente.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **todasLasFotos**: Opcional. Si se selecciona *Sí*, se muestran todas las fotos del docente. La opciones *No* y *No establecido* devuelven la más reciente (**idFoto** en *XPE_FotosPersonal* = **idFotoReciente** en *XPE_IdentificacionCentros*).

**Observaciones**:
* Opción 1: El *codigoCentro* es obligatorio, además de uno solo de los campos *nifNie* o *pasaporte*.
* Opción 2: Se debe indicar uno solo de los campos *idDocenteCentro* o *idDocenteServicio*.

## Parámetros específicos.

### Opción 1.
* **codigoCentro**: Obligatorio (Ej. 35010488).
* **nifNie**: Obligatorio si no se indica pasaporte.
* **pasaporte**: Obligatorio si no se indica nifNie.

**Observaciones**: Los campos *idDocenteCentro* e *idDocenteServicio* no están permitidos en esta opción.

### Opción 2.
* **idDocenteCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idDocenteServicio**: Obligatorio (Ej. 2AA7983F81C74285B41875018751C91D).

**Observaciones**: Solo se debe indicar uno de los parámetros. Los campos *codigoCentro*, *nifNie* y *pasaporte* no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todas las fotos del docente con NIF "11000000C" del centro con código "35010488".
* /gestionacadcentros/docentes/fotos?opcion=1 & codigoCentro=35010488 & nifNie=11000000C & todasLasFotos=true

### B) Solicitud de la foto más reciente del docente con idDocenteServicio = "D1269A4D5DE6436EA1762F55B2E0E9C3".
* /gestionacadcentros/docentes/fotos?opcion=2 & idDocenteServicio=D1269A4D5DE6436EA1762F55B2E0E9C3
