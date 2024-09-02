# Descripción general

Este endpoint proporciona las fotos del alumnado que figuran en su expediente.

## Parámetros comunes

* **todasLasFotos**: Opcional. Si se selecciona "Sí", se muestran todas las fotos del expediente del alumnado. La opciones "No" y "No establecido" devuelven la más reciente (idFoto en XAL_FotosAlumnos = idFotoReciente en XAL_AlumnadoCentro).

**Observaciones**:
* Opción 1: El *codigoCentro* es obligatorio, además de uno solo de los campos *cial*, *nifNie* o *pasaporte*.
* Opción 2: Se debe indicar uno solo de los campos *idAlumnadoCentro* o *idMatricula*.

## Parámetros específicos

### Opción 1
* **codigoCentro**: Obligatorio (Ej. 35010488).
* **cial**: CIAL del alumnado.
* **nifNie**: NIF o NIE del alumnado.
* **pasaporte**: Pasaporte del alumnado.

**Observaciones**: Los campos idAlumnadoCentro e idMatricula no están permitidos en esta opción.

### Opción 2
* **idAlumnadoCentro**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).
* **idMatricula**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).

**Observaciones**: Solo se debe indicar uno de los parámetros. Los campos codigoCentro, cial, nifNie y pasaporte no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todas las fotos del alumnado del centro con código "35010488" y pasaporte "119227796".
* ?opcion=1 & codigoCentro=35010488 & pasaporte=119227796 & todasLasFotos=true

### B) Solicitud de la foto más reciente del alumnado con idAlumnadoCentro = "EA1EF2E1-E86B-42F5-A659-1152F745EF37".
* ?opcion=2 & idAlumnadoCentro=EA1EF2E1-E86B-42F5-A659-1152F745EF37
