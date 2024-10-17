
# Descripción general.

Este endpoint devuelve todas las evaluaciones correspondientes a una enseñanza concreta  (Ej. *Educación Primaria*, *Ciclos Formativos de Grado Básico*, *Bachillerato*, etc.) a partir del parámetro _idEnsenyanza_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idEnsenyanza**: Obligatorio (Ej. e3604da5156e4470a5a3aff7ab987ece).

# Ejemplos.
### A) Solicitud de datos de las evaluaciones para la enseñanza con idEnsenyanza = "e3604da5156e4470a5a3aff7ab987ece".
* /gestionacadcentros/ensenyanzas/e3604da5156e4470a5a3aff7ab987ece/evaluaciones
