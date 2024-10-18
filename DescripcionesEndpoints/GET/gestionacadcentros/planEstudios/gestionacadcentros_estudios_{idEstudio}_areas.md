
# Descripción general.

Este endpoint proporciona las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de un estudio concreto a partir del parámetro *idEstudio*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **incluirNoVigentes**: Si se selecciona, incluye las áreas no vigentes. Si se escoge "No" o "No establecido", devuelve solo las áreas vigentes.
* **nivelDetalle**: Se deberá escoger uno obligatoriamente r, m (reducido, medio).

## Parámetros específicos.

* **idEstudio**: Obligatorio (Ej. e3a3a508746942ab86a719ed52797063).

# Ejemplos.
### A) Solicitud de las áreas (incluidas las no vigentes) con nivelDetalle *medio* del estudio con idEstudio = "136b08ac56f74175b01324f7f5ddaaf9".
* /gestionacadcentros/estudios/136b08ac56f74175b01324f7f5ddaaf9/areas?incluirNoVigentes=true & nivelDetalle=m

### B) Solicitud de las áreas vigentes con nivelDetalle *reducido* del estudio con idEstudio = "8c584333c4074a64b82db54f74defee4".
* /gestionacadcentros/estudios/8c584333c4074a64b82db54f74defee4/areas?nivelDetalle=r

