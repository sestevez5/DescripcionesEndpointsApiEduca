
# Descripción general.

Este endpoint devuelve todas las evaluaciones correspondientes a un curso escolar concreto a partir del parámetro _idCursoCentro_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. 9854621FA899438C8818780A9C364044).

# Ejemplos.
### A) Solicitud de datos de las evaluaciones para el curso escolar con idCursoCentro = "9854621FA899438C8818780A9C364044".
* /gestionacadcentros/cursos-centros/9854621FA899438C8818780A9C364044/evaluaciones


* /gestionacadcentros/cursos-centros/9854621FA899438C8818780A9C364044/evaluaciones?idEnsenyanza=3175495d4e6f4c8d8bf3a5c22c5195b0
