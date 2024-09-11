# Descripción general.

Este endpoint proporciona las diferentes dependencias (Aulas, salas, talleres, etc.) que conforman un centro educativo a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), el campo *idCursoCentro* es obligatorio.

## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237-EC8C-4AFF-A870-01C277A3D712)

# Ejemplo.
### A) Solicitud de las dependencias para el idCursoCentro "E480D237-EC8C-4AFF-A870-01C277A3D712".
* E480D237-EC8C-4AFF-A870-01C277A3D712/dependencias
