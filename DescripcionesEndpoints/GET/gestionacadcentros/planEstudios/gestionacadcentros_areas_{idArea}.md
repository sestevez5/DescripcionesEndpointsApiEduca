# Descripción general.

Este endpoint proporciona información de las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de los diferentes estudios de un centro educativo a partir del parámetro *idArea*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.

## Parámetros específicos.

### Opción 1.
* **idArea**: Obligatorio (Ej. 2023).





# Ejemplos.
### A) Solicitud de datos con nivelDetalle medio para los estudios de una enseñanza concreta y un idCursoCentro determinado.
* ?opcion=2 & idCursoCentro=561BD9BC-E680-49DA-ABE9-0F3BA098D444 & idEnsenyanza=0B2E6A87-262D-4502-B8EB-834F44F60488 & nivelDetalle=m

### B) Solicitud de datos con nivelDetalle reducido de todos los estudios y enseñanzas del centro con código "35010488" en el curso 2022.
* ?opcion=1 & cursoEscolar=2022 & codigoCentro=35010488 & nivelDetalle=r

### C) Solicitud de datos con niveDetalle medio de los estudios de una enseñanza concreta del centro con código "35010488" en el curso 2023. 
* ?opcion=1 & cursoEscolar=2023 & codigoCentro=35010488 & idEnsenyanza=737B55AB-E9C8-4EF0-A923-21B7E63C6F6B & idEstudio=016FE156-2D80-44BC-AA11-00652E182F90 & nivelDetalle=m
