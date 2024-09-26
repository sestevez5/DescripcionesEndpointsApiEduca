# modificándose


# Descripción general.

Este endpoint devuelve los datos de los docentes de un centro educativo a partir del parámetro _idCentro_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 561EBA45-51E5-4E3F-BA6B-C4CBB8363079)
* **tieneServicioEnElCentro**: Booleano que permite seleccionar a los docentes que tienen o han tenido algún servicio en el centro. Si no se indica, se seleccionan todos los docentes del centro.
* **tieneServicioEnElCurso**: Cuando se ha seleccionado la opción anterior, permite indicar el curso escolar en el que ha tenido servicio un docente (Ej. 2023).

# Ejemplos.
### A) Solicitud de datos extendidos del docente con nif = 00000001R en el centro con código "35010488".
* ?opcion=1 & codigoCentro=35010488 & nifnie=00000001R & nivelDetalle=e

### B) Solicitud de datos reducidos de todos los docentes del centro con código "35010488".
* ?opcion=2 & codigoCentro=35010488

### C) Solicitud de datos con nivel de detalle medio de los docentes del centro con código "35010488" y servicio en el curso 2023. 
* ?opcion=2 & codigoCentro=35010488 & tieneServicioEnElCentro=true & tieneServicioEnElCurso=2023 & nivelDetalle=m

