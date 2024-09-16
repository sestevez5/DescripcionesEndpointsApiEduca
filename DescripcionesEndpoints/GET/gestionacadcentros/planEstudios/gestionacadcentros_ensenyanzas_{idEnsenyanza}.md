# Descripción general.

Este endpoint proporciona las enseñanzas impartidas en un centro educativo (Ej. Educación Secundaria Obligatoria, Ciclos Formativos de Grado Medio, etc.) a partir del parámetro *idEnsenyanza*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, incluye las enseñanzas no vigentes. Si se escoge "No" o "No establecido", devuelve solo las enseñanzas vigentes.

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4)

# Ejemplos.
### A) Solicitud de las enseñanzas con idEnsenyanza = "9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4".
* 9bba0d43-3be7-4d0c-b8ba-14b13ab63ad4

