# Descripción general.

Este endpoint devuelve las evaluaciones de un centro educativo a partir del parámetro _idEvaluacion_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idEvaluacion**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud de las evaluaciones del curso 2019 para una enseñanza concreta del centro con código "35010488".
* /gestionacadcentros/evaluaciones?opcion=1 & cursoEscolar=2019 & codigoCentro=35010488 & idEnsenyanza=C3E9383D03D94CD183CE15DAF8BF3E1D

### B) Solicitud de todas las evaluaciones para el idCursoCentro especificado .
* /gestionacadcentros/evaluaciones?opcion=2 & idCursoCentro=E480D237EC8C4AFFA87001C277A3D712

### C) Solicitud de las evaluaciones de una enseñanza concreta para un idCursoCentro determinado.
* /gestionacadcentros/evaluaciones?opcion=2 & idCursoCentro=E480D237EC8C4AFFA87001C277A3D712 & idEnsenyanza=FF31EB108792412187C73076537F5822
