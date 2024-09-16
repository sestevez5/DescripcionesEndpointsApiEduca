# Descripción general.

Este endpoint proporciona los estudios impartidos en un centro educativo (Ej. 3º Educación Secundaria Obligatoria, 1º CFGM Informática y Comunicaciones, etc.) a partir del parámetro *idEnsenyanza*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo.

## Parámetros específicos.



# Ejemplos.
### A) Solicitud de los estudios, incluidos los no ofertados, para el idCursoCentro especificado .
* ?opcion=2 & incluirNoOfertados=true & idCursoCentro=0D95CCCE-E390-4190-B1F8-10A90A4B7477

### B) Solicitud de todos los estudios del centro con código "38016519" en el curso 2022.
* ?opcion=1 & cursoEscolar=2022 & codigoCentro=38016519
