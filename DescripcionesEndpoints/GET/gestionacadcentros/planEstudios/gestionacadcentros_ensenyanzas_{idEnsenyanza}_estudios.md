# Descripción general.

Este endpoint proporciona los estudios impartidos en un centro educativo (Ej. *3º Educación Secundaria Obligatoria*, *1º CFGM Informática y Comunicaciones*, etc.) a partir del parámetro *idEnsenyanza*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo. Si se escoge "No" o "No establecido", devuelve solo los estudios ofertados.

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d433be74d0cb8ba14b13ab63ad4).

# Ejemplos.
### A) Solicitud de los estudios vigentes y ofertados correspondientes a la enseñanza con idEnsenyanza = "9bba0d433be74d0cb8ba14b13ab63ad4".
* /gestionacadcentros/ensenyanzas/9bba0d433be74d0cb8ba14b13ab63ad4/estudios

### B) Solicitud de los estudios, incluyendo los no vigentes y no ofertados, correspondientes a la enseñanza con idEnsenyanza = "a0361e9f3fc6434ba16def492101d8f1".
* /gestionacadcentros/ensenyanzas/a0361e9f3fc6434ba16def492101d8f1/estudios?incluirNoVigentes=true & incluirNoOfertados=true

