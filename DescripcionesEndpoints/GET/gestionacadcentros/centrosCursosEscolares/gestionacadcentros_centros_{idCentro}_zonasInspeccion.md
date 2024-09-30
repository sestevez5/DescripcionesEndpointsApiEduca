# Descripción general.

Este endpoint devuelve información relativa a la zona de inspección (inspector, telefonoInspeccion, diaGuardia, etc.) correspondiente a un centro educativo a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 3793A6D1C74242EDB005DA3529421EE5)
* **cursoEscolar**: Obligatorio (Ej. 2023).

# Ejemplos.
### A) Solicitud de la zona de inspección del centro con idCentro = "561EBA4551E54E3FBA6BC4CBB8363079" para el curso "2024".
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/zonas-inspeccion?cursoEscolar=2024
