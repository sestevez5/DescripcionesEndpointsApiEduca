# Descripción general.

Este endpoint devuelve información relativa a los cargos y funciones (dirección, jefatura, coordinaciones, etc.) de un centro educativo a partir de su _codigoCentro_.

## Parámetros comunes.
* **codigoCentro**: Obligatorio (Ej. 38010773)
* **cursoEscolar**: Obligatorio (2021)
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: El campo idCursoCentro no está permitido en esta opción.


# Ejemplos.
### A) Solicitud de todas las enseñanzas para el idCursoCentro especificado .
* ?opcion=2 & idCursoCentro=E480D237-EC8C-4AFF-A870-01C277A3D712

### B) Solicitud de todas las enseñanzas del centro con código "35007374" en el curso 2024.
* ?opcion=1 & cursoEscolar=2024 & codigoCentro=35007374



**Observaciones**: Debe cumplimentarse solamente uno de ellos.

### Opción 2.
* **tieneServicioEnElCentro**: Booleano que permite seleccionar a los docentes que tienen o han tenido algún servicio en el centro. Si no se indica, se seleccionan todos los docentes del centro.
* **tieneServicioEnElCurso**: Cuando se ha seleccionado la opción anterior, permite indicar el curso escolar en el que ha tenido servicio un docente (Ej. 2023).

**Observaciones**: Ambos son opcionales.
