
# Descripción general.

Este endpoint devuelve todas las evaluaciones correspondientes a un curso escolar concreto a partir del parámetro _idCursoCentro_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. 9854621FA899438C8818780A9C364044).
* **idEnsenyanza**: Si se indica, se muestran solo las evaluaciones correspondientes a la enseñanza especificada (Ej. 3175495d4e6f4c8d8bf3a5c22c5195b0).

# Ejemplos.
### A) Solicitud de datos de las evaluaciones para el curso escolar con idCursoCentro = "9854621FA899438C8818780A9C364044".
* /gestionacadcentros/cursos-centros/9854621FA899438C8818780A9C364044/evaluaciones

### B) Solicitud de datos de las evaluaciones de la enseñanza con idEnsenyanza = "3175495d4e6f4c8d8bf3a5c22c5195b0" para el curso escolar con idCursoCentro = "9854621FA899438C8818780A9C364044".
* /gestionacadcentros/cursos-centros/9854621FA899438C8818780A9C364044/evaluaciones?idEnsenyanza=3175495d4e6f4c8d8bf3a5c22c5195b0
