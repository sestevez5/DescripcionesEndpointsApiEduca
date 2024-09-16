# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ámbito de Comunicación y Representación*, *Física y Química*, *Atención al cliente*, etc.) de las diferentes enseñanzas y estudios de un centro educativo.

## Parámetros comunes.

* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo los estudios vigentes.
* **incluirNoOFertados**: Si se selecciona, incluye los estudios no ofertados por el centro educativo. Si se escoge "No" o "No establecido", devuelve solo los estudios ofertados.

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4).
* **idEstudio**: Si no se indica, se muestran todas los estudios para el curso y centro indicado.

# Ejemplos.
### A) Solicitud de los estudios vigentes y ofertados correspondientes a la enseñanza con idEnsenyanza = "9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4".
* 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4/estudios

### B) Solicitud de los estudios, incluyendo los no vigentes y no ofertados, correspondientes a la enseñanza con idEnsenyanza = "a0361e9f-3fc6-434b-a16d-ef492101d8f1".
a0361e9f-3fc6-434b-a16d-ef492101d8f1/estudios?incluirNoVigentes=true & incluirNoOfertados=true
