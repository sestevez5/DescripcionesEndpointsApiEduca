Este parámetro establece el conjunto de parámetros válido para cada 'opcion'.

Parámetros habilitados para 'opcion = 1': 

* codigoCentro (_obligatorio_)
* todasLasFotos (_obligatorio_)
* cial\r\n* nifNie 
* pasaporte

> (_Además, es necesario especificar uno y sólo uno de los parámetros cial, nifNie o pasaporte_)

Parámetros habilitados para 'opcion = 2':

* idAlumnadoCentro (_obligatorio_)
* todasLasFotos (_obligatorio_)

# Descripción general

Este endpoint proporciona las fotos del alumnado que figuran en su expediente.

**Observaciones**:
* Opción 1: El *codigoCentro* es obligatorio, además de uno solo de los campos *cial*, *nifNie* o *pasaporte*.
* Opción 2: Se debe indicar uno solo de los campos *idAlumnadoCentro* o *idMatricula*.
* Además del codigoCentro, será necesario indicarcodigoCentro.
Los campos idAlumnadoCentro e idMatricula no están permitido en esta opción.

## Parámetros específicos

### Opción 1
* **codigoCentro**: Obligatorio (Ej. 35010488).
* **cial**: CIAL del alumnado.
* **nifNie**: NIF o NIE del alumnado.
* **pasaporte**: Pasaporte del alumnado.

**Observaciones**: Los campos idAlumnadoCentro e idMatricula no están permitido en esta opción.

### Opción 2
* **idAlumnadoCentro**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).
* **idMatricula**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).

**Observaciones**: Los campos cursoEscolar y codigoCentro no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle medio para los estudios de una enseñanza concreta y un idCursoCentro determinado.
* ?opcion=2 & idCursoCentro=561BD9BC-E680-49DA-ABE9-0F3BA098D444 & idEnsenyanza=0B2E6A87-262D-4502-B8EB-834F44F60488 & nivelDetalle=m

### B) Solicitud de datos con nivelDetalle reducido de todos los estudios y enseñanzas del centro con código "35010488" en el curso 2022.
* ?opcion=1 & cursoEscolar=2022 & codigoCentro=35010488 & nivelDetalle=r

### C) Solicitud de datos con niveDetalle medio de los estudios de una enseñanza concreta del centro con código "35010488" en el curso 2023. 
* ?opcion=1 & cursoEscolar=2023 & codigoCentro=35010488 & idEnsenyanza=737B55AB-E9C8-4EF0-A923-21B7E63C6F6B & idEstudio=016FE156-2D80-44BC-AA11-00652E182F90 & nivelDetalle=m
