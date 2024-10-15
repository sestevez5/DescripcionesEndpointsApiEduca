# Descripción general.

Este endpoint proporciona todos los docentes de un determinado centro educativo en un curso escolar a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *idCursoCentro* es obligatorio.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712)
* **fechaReferencia**: Devuelve solo los docentes con nombramiento vigente en esa fecha (Ej. 2024-10-10). Si no se indica, suministra todos los docentes con servicio en el centro y curso especificado.

# Ejemplo.
### A) Solicitud de datos de los docentes con nombramiento vigente a fecha "07/03/2024" para el idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/cursos-centros/E480D237EC8C4AFFA87001C277A3D712/docentes-servicios?fechaReferencia=2024-03-07

### B) Solicitud de datos de todos los docentes para el idCursoCentro = "5C08325B4B744F328977628385331092".
* /gestionacadcentros/cursos-centros/5C08325B4B744F328977628385331092/docentes-servicios
