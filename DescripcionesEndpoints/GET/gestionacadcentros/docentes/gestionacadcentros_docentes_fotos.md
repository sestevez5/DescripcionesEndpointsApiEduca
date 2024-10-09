Este parámetro establece el conjunto de parámetros válido para cada 'opcion'.

Parámetros habilitados para 'opcion = 1': 

* codigoCentro (_obligatorio_)
* todasLasFotos (_obligatorio_)
* nifNie 
* pasaporte

> (_Además, es necesario especificar uno y sólo uno de los parámetros nifNie o pasaporte_)

Parámetros habilitados para 'opcion = 2': 

* idDocenteCentro (_obligatorio_)
* todasLasFotos (_obligatorio_)




# Descripción general.

Este endpoint proporciona las fotos del personal docente.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **todasLasFotos**: Opcional. Si se selecciona "Sí", se muestran todas las fotos del docente. La opciones "No" y "No establecido" devuelven la más reciente (**idFoto** en *XPE_FotosPersonal* = **idFotoReciente** en *XPE_IdentificacionCentros*).

**Observaciones**:
* Opción 1: El *codigoCentro* es obligatorio, además de uno solo de los campos *nifNie* o *pasaporte*.
* Opción 2: Se debe indicar uno solo de los campos *idDocenteCentro* o *idDocenteServicio*.

## Parámetros específicos.

### Opción 1.
* **codigoCentro**: Obligatorio (Ej. 35010488).
* **cial**: CIAL del alumnado.
* **nifNie**: NIF o NIE del alumnado.
* **pasaporte**: Pasaporte del alumnado.

**Observaciones**: Los campos idAlumnadoCentro e idMatricula no están permitidos en esta opción.

### Opción 2.
* **idAlumnadoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idMatricula**: Obligatorio (Ej. 2AA7983F81C74285B41875018751C91D).

**Observaciones**: Solo se debe indicar uno de los parámetros. Los campos codigoCentro, cial, nifNie y pasaporte no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todas las fotos del alumnado con pasaporte "119227796" del centro con código "35010488".
* /gestionacadcentros/alumnado/fotos?opcion=1 & codigoCentro=35010488 & pasaporte=119227796

### B) Solicitud de la foto más reciente del alumnado con idAlumnadoCentro = "EA1EF2E1E86B42F5A6591152F745EF37".
* /gestionacadcentros/alumnado/fotos?opcion=2 & idAlumnadoCentro=EA1EF2E1E86B42F5A6591152F745EF37
