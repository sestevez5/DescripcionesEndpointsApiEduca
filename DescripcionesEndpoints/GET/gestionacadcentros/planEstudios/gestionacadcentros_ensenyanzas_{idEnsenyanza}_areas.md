# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de las diferentes enseñanzas y estudios de un centro educativo.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).
* **idEnsenyanza**: Si no se indica, se muestran todas las enseñanzas para el curso y centro indicado.
* **idEstudio**: Si no se indica, se muestran todas los estudios para el curso y centro indicado.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.


Este endpoint proporciona los estudios impartidos en un centro educativo (Ej. *3º Educación Secundaria Obligatoria*, *1º CFGM Informática y Comunicaciones*, etc.) a partir del parámetro *idEnsenyanza*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo. Si se escoge "No" o "No establecido", devuelve solo los estudios ofertados.

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4).

# Ejemplos.
### A) Solicitud de los estudios vigentes y ofertados correspondientes a la enseñanza con idEnsenyanza = "9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4".
* 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4/estudios

### B) Solicitud de los estudios, incluyendo los no vigentes y no ofertados, correspondientes a la enseñanza con idEnsenyanza = "a0361e9f-3fc6-434b-a16d-ef492101d8f1".
a0361e9f-3fc6-434b-a16d-ef492101d8f1/estudios?incluirNoVigentes=true & incluirNoOfertados=true
