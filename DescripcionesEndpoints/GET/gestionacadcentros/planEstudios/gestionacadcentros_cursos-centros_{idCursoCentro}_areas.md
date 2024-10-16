
# Descripción general.

Este endpoint proporciona la colección de áreas (Ej. *Ámbito de Comunicación y Representación*, *Física y Química*, *Atención al cliente*, etc.) ofertadas en el plan de estudios de un centro educativo en un curso escolar a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, permite incluir áreas pertenecientes a estudios no vigentes ofertados por el centro. Si se escoge "No" o "No establecido", devuelve solo áreas de estudios vigentes.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idEnsenyanza**: Si se indica, se muestran solo las áreas de la enseñanza especificada (Ej. 1a50607b61824997b4ef85388481a218).
* **idEstudio**: Si se indica, se muestran solo las áreas del estudio especificado (Ej. 380c4b19e1f6408aad67141c869f69ff).

# Ejemplos.
### A) Solicitud con nivel de detalle *reducido* de las áreas de estudios vigentes correspondientes al estudio con idEstudio = "b9fbae1ae1754ac1bee1228baaa597ed" de la enseñanza con idEnsenyanza = "1a50607b61824997b4ef85388481a218" en el curso con idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/cursos-centros/E480D237EC8C4AFFA87001C277A3D712/areas?idEnsenyanza=1a50607b61824997b4ef85388481a218 & idEstudio=b9fbae1ae1754ac1bee1228baaa597ed & nivelDetalle=r

### B) Solicitud con nivel de detalle *medio* de todas las áreas, incluyendo las de estudios no vigentes, correspondientes al curso con idCursoEscolar = "391C57574CE843CFB45F08CA129F6FBB".
* /gestionacadcentros/cursos-centros/391C57574CE843CFB45F08CA129F6FBB/areas?incluirNoVigentes=true & nivelDetalle=m
