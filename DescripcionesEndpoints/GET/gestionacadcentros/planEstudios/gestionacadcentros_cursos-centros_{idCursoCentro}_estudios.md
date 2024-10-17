# Descripción general.

Este endpoint proporciona los estudios impartidos en un centro educativo (Ej. *3º Educación Secundaria Obligatoria*, *1º CFGM Informática y Comunicaciones*, etc.) a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo. Si se escoge "No" o "No establecido", devuelve solo los estudios ofertados.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. 3BCA095B8AEC4939BAB14E9FDAFA4A41).

# Ejemplos.
### A) Solicitud de los estudios vigentes y ofertados en el curso con idCursoEscolar = "3BCA095B8AEC4939BAB14E9FDAFA4A41".
* /gestionacadcentros/cursos-centros/3BCA095B8AEC4939BAB14E9FDAFA4A41/estudios

### B) Solicitud de los estudios, incluyendo los no ofertados, correspondientes al curso con idCursoEscolar = "5C08325B4B744F328977628385331092".
* /gestionacadcentros/cursos-centros/5C08325B4B744F328977628385331092/estudios?incluirNoOfertados=true
