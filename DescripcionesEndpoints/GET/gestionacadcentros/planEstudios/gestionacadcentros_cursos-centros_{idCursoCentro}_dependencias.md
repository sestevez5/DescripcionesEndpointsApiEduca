# Descripción general.

Este endpoint proporciona las diferentes dependencias (Aulas, salas, talleres, etc.) que conforman un centro educativo a partir del parámetro *idCursoCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *idCursoCentro* es obligatorio.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712)

# Ejemplo.
### A) Solicitud de las dependencias para el idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/cursos-centros/E480D237EC8C4AFFA87001C277A3D712/dependencias
