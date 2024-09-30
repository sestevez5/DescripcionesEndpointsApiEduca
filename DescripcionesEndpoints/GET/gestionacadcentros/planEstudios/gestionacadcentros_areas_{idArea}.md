# Descripción general.

Este endpoint proporciona información exhaustiva de las áreas (Ej. *Ciencias de la Naturaleza*, *Literatura Universal*, *Formación en Centros de Trabajo*, etc.) de los diferentes estudios de un centro educativo a partir del parámetro *idArea*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, permite incluir áreas pertenecientes a estudios no vigentes ofertados por el centro. Si se escoge "No" o "No establecido", devuelve solo áreas de estudios vigentes.

## Parámetros específicos.

* **idArea**: Obligatorio (Ej. 5e09f10d778a4b8ab98bb9495b050018).

# Ejemplo.
### A) Solicitud de datos del área con idArea = "5e09f10d778a4b8ab98bb9495b050018".
* /gestionacadcentros/areas/5e09f10d778a4b8ab98bb9495b050018
