# Descripción general

Este endpoint proporciona información de las áreas de las diferentes enseñanzas y estudios de un centro educativo.

## Parámetros comunes

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio)
* **idEnsenyanza**: Si no se indica, se muestran todas las enseñanzas para el curso y centro indicado.
* **idEstudio**: Si no se indica, se muestran todas los estudios para el curso y centro indicado.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes.

**Observaciones**:
>* En las dos opciones el nivelDetalle es obligatorio.
>* Opción 1: Los campos obligatorios son el cursoEscolar y el codigoCentro.
>* Opción 2: El campo idCursoCentro es obligatorio.

## Parámetros específicos

### Opción 1
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: El campo idCursoCentro no está permitido en esta opción.

### Opción 2
* **idCursoCentro**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712).

**Observaciones**: Los campos cursoEscolar y codigoCentro no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle medio para los estudios de una enseñanza concreta y un idCursoCentro determinado.
> * ?opcion=2 & idCursoCentro=561BD9BC-E680-49DA-ABE9-0F3BA098D444 & idEnsenyanza=0B2E6A87-262D-4502-B8EB-834F44F60488 & nivelDetalle=m

### B) Solicitud de datos con nivelDetalle reducido de todos los estudios y enseñanzas del centro con código "35010488" en el curso 2022.
> * ?opcion=1 & cursoEscolar=2022 & codigoCentro=35010488 & nivelDetalle=r

### C) Solicitud de datos con niveDetalle medio de los estudios de una enseñanza concreta del centro con código "35010488" en el curso 2023. 
> * ?opcion=1 & cursoEscolar=2023 & codigoCentro=35010488 & idEnsenyanza=737B55AB-E9C8-4EF0-A923-21B7E63C6F6B & idEstudio=016FE156-2D80-44BC-AA11-00652E182F90 & nivelDetalle=m
