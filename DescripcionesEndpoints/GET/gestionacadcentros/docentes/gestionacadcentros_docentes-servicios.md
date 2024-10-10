# Modificar modificar modificar


# Descripción general.

Este endpoint proporciona todos los nombramientos docentes para un curso escolar o los de un determinado docente en un centro educativo según la opción y parámetros escogidos.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.

**Observaciones**:
* Opción 1: Además del *cursoEscolar*, será necesario indicar el *codigoCentro*.
* Opción 2: Solo debe cumplimentarse uno de los parámetros *nifNie* o *pasaporte*.

## Parámetros específicos.

### Opción 1.

* **cursoEscolar**: Obligatorio (Ej. 2022).
* **codigoCentro**: Obligatorio (Ej. 35009139).
* **fechaReferencia**: Devuelve solo los nombramientos vigentes en esa fecha (Ej. 2024-10-10). Si no se indica, suministra todos los nombramientos en el curso especificado.

### Opción 2.
* **nifnie**: NIF o NIE del docente.
* **pasaporte**: Pasaporte del docente.

# Ejemplos.
### A) Solicitud de datos extendidos del docente con nif = 00000001R en el centro con código "35010488".
* /gestionacadcentros/docentes?opcion=1 & codigoCentro=35010488 & nifnie=00000001R & nivelDetalle=e

### B) Solicitud de datos reducidos de todos los docentes del centro con código "35010488".
* /gestionacadcentros/docentes?opcion=2 & codigoCentro=35010488

### C) Solicitud de datos con nivel de detalle medio de los docentes del centro con código "35010488" y servicio en el curso 2023. 
* /gestionacadcentros/docentes?opcion=2 & codigoCentro=35010488 & tieneServicioEnElCentro=true & tieneServicioEnElCurso=2023 & nivelDetalle=m







## Parámetros específicos.

* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712)
* **fechaReferencia**: Devuelve solo los docentes con nombramiento vigente en esa fecha (Ej. 2024-10-10). Si no se indica, suministra todos los docentes con servicio en el centro y curso especificado.

# Ejemplo.
### A) Solicitud de datos de los docentes con nombramiento vigente a fecha "07/03/2024" para el idCursoCentro "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/cursos-centros/E480D237EC8C4AFFA87001C277A3D712/docentes-servicios?fechaReferencia=2024-03-07

### B) Solicitud de datos de todos los docentes para el idCursoCentro "5C08325B4B744F328977628385331092".
* /gestionacadcentros/cursos-centros/5C08325B4B744F328977628385331092/docentes-servicios
