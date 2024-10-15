# MODIFICAR
# MODIFICAR
# MODIFICAR

136b08ac56f74175b01324f7f5ddaaf9

# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de un estudio concreto a partir del parámetro *idEstudio*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.


## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d433be74d0cb8ba14b13ab63ad4).

# Ejemplos.
### A) Solicitud de los estudios vigentes y ofertados correspondientes a la enseñanza con idEnsenyanza = "9bba0d433be74d0cb8ba14b13ab63ad4".
* /gestionacadcentros/ensenyanzas/9bba0d433be74d0cb8ba14b13ab63ad4/estudios

### B) Solicitud de los estudios, incluyendo los no vigentes y no ofertados, correspondientes a la enseñanza con idEnsenyanza = "a0361e9f3fc6434ba16def492101d8f1".
/gestionacadcentros/ensenyanzas/a0361e9f3fc6434ba16def492101d8f1/estudios?incluirNoVigentes=true & incluirNoOfertados=true

# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de las diferentes enseñanzas y estudios de un centro educativo.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).
* **idEnsenyanza**: Si no se indica, se muestran todas las enseñanzas para el curso y centro indicado.
* **idEstudio**: Si no se indica, se muestran todas los estudios para el curso y centro indicado.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.

**Observaciones**:
* En las dos opciones el nivelDetalle es obligatorio.
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
### A) Solicitud de datos con nivelDetalle medio para los estudios de una enseñanza concreta y un idCursoCentro determinado.
* /gestionacadcentros/areas?opcion=2 & idCursoCentro=561BD9BCE68049DAABE90F3BA098D444 & idEnsenyanza=0B2E6A87262D4502B8EB834F44F60488 & nivelDetalle=m

### B) Solicitud de datos con nivelDetalle reducido de todos los estudios y enseñanzas del centro con código "35010488" en el curso 2022.
* /gestionacadcentros/areas?opcion=1 & cursoEscolar=2022 & codigoCentro=35010488 & nivelDetalle=r

### C) Solicitud de datos con niveDetalle medio de los estudios de una enseñanza concreta del centro con código "35010488" en el curso 2023. 
* /gestionacadcentros/areas?opcion=1 & cursoEscolar=2023 & codigoCentro=35010488 & idEnsenyanza=737B55ABE9C84EF0A92321B7E63C6F6B & idEstudio=016FE1562D8044BCAA1100652E182F90 & nivelDetalle=m


