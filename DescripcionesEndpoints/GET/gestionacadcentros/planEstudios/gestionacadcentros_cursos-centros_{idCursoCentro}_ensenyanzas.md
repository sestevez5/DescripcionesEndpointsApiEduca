# Descripción general.

Este endpoint devuelve las enseñanzas impartidas en los centros educativos (Ej. *Educación Primaria*, *Ciclos Formativos de Grado Básico*, *Bachillerato*, etc.) a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros..

## Parámetros comunes.

* **incluirNoVigentes**: Si se selecciona, incluye las enseñanzas no vigentes. Si se escoge "No" o "No establecido", devuelve solo las enseñanzas vigentes.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).

# Ejemplos.
### A) Solicitud de las enseñanzas vigentes para el idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/cursos-centros/E480D237EC8C4AFFA87001C277A3D712/ensenyanzas
