# Descripción general.

Este endpoint proporciona las fotos del alumnado que figuran en su expediente.

## Parámetros comunes.

* **todasLasFotos**: Opcional. Si se selecciona "Sí", se muestran todas las fotos del expediente del alumnado. La opciones "No" y "No establecido" devuelven la más reciente (**idFoto** en *XAL_FotosAlumnos* = **idFotoReciente** en *XAL_AlumnadoCentro*).

**Observaciones**:
* Opción 1: El *codigoCentro* es obligatorio, además de uno solo de los campos *cial*, *nifNie* o *pasaporte*.
* Opción 2: Se debe indicar uno solo de los campos *idAlumnadoCentro* o *idMatricula*.

## Parámetros específicos.

### Opción 1.
* **codigoCentro**: Obligatorio (Ej. 35010488).
* **cial**: CIAL del alumnado.
* **nifNie**: NIF o NIE del alumnado.
* **pasaporte**: Pasaporte del alumnado.

**Observaciones**: Los campos *idAlumnadoCentro* e *idMatricula* no están permitidos en esta opción.

### Opción 2.
* **idAlumnadoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idMatricula**: Obligatorio (Ej. 2AA7983F81C74285B41875018751C91D).

**Observaciones**: Solo se debe indicar uno de los parámetros. Los campos *codigoCentro*, *cial*, *nifNie* y *pasaporte* no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todas las fotos del alumnado con pasaporte "119227796" del centro con código "35010488".
* /gestionacadcentros/alumnado/fotos?opcion=1 & codigoCentro=35010488 & pasaporte=119227796

### B) Solicitud de la foto más reciente del alumnado con idAlumnadoCentro = "EA1EF2E1E86B42F5A6591152F745EF37".
* /gestionacadcentros/alumnado/fotos?opcion=2 & idAlumnadoCentro=EA1EF2E1E86B42F5A6591152F745EF37
