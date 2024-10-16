# MODIFICAR
# MODIFICAR
# MODIFICAR


# Descripción general.

Este endpoint proporciona la colección de áreas (Ej. *Ámbito de Comunicación y Representación*, *Física y Química*, *Atención al cliente*, etc.) ofertadas en el plan de estudios de  un centro educativo en un curso escolar a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, permite incluir áreas pertenecientes a estudios no vigentes ofertados por el centro. Si se escoge "No" o "No establecido", devuelve solo áreas de estudios vigentes.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idEnsenyanza**: Si se indica, se muestran solo las áreas de la enseñanza especificada (Ej. 9bba0d433be74d0cb8ba14b13ab63ad4).
* **idEstudio**: Si se indica, se muestran solo las áreas del estudio especificado (Ej. 380c4b19e1f6408aad67141c869f69ff).

# Ejemplos.
### A) Solicitud con nivel de detalle *medio* de las áreas correspondientes al estudio con idEstudio = "c7200149ef644b799522af86214669dc" de la enseñanza con idEnsenyanza = "70d15bce1e77481db9582f3215f1071a".
* /gestionacadcentros/ensenyanzas/70d15bce1e77481db9582f3215f1071a/areas?idEstudio=c7200149ef644b799522af86214669dc & nivelDetalle=m

### B) Solicitud con nivel de detalle *reducido* de todas las áreas, incluyendo las de estudios no vigentes, correspondientes a la enseñanza con idEnsenyanza = "70d15bce1e77481db9582f3215f1071a".
* /gestionacadcentros/ensenyanzas/70d15bce1e77481db9582f3215f1071a/areas?incluirNoVigentes=true & nivelDetalle=r



# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ámbito de Comunicación y Representación*, *Física y Química*, *Atención al cliente*, etc.) de las diferentes enseñanzas de un centro educativo a partir del parámetro *idEnsenyanza*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, permite incluir áreas pertenecientes a estudios no vigentes ofertados por el centro. Si se escoge "No" o "No establecido", devuelve solo áreas de estudios vigentes.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. 9bba0d433be74d0cb8ba14b13ab63ad4).
* **idEstudio**: Si se indica, se muestran solo las áreas del estudio indicado (Ej. c7200149ef644b799522af86214669dc).

# Ejemplos.
### A) Solicitud con nivel de detalle *medio* de las áreas correspondientes al estudio con idEstudio = "c7200149ef644b799522af86214669dc" de la enseñanza con idEnsenyanza = "70d15bce1e77481db9582f3215f1071a".
* /gestionacadcentros/ensenyanzas/70d15bce1e77481db9582f3215f1071a/areas?idEstudio=c7200149ef644b799522af86214669dc & nivelDetalle=m

### B) Solicitud con nivel de detalle *reducido* de todas las áreas, incluyendo las de estudios no vigentes, correspondientes a la enseñanza con idEnsenyanza = "70d15bce1e77481db9582f3215f1071a".
* /gestionacadcentros/ensenyanzas/70d15bce1e77481db9582f3215f1071a/areas?incluirNoVigentes=true & nivelDetalle=r
