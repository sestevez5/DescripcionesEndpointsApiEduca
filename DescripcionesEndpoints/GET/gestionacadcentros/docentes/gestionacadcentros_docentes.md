# Descripción general.

Este endpoint devuelve los datos de los docentes a partir del código del centro.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente
* **codigoCentro**: Obligatorio (Ej. 38010773)
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

**Observaciones**:
* Opción 1: Además del codigoCentro, será necesario indicar nifnie o pasaporte.
* Opción 2: Además del codigoCentro, opcionalmente se podrá seleccionar tieneServicioEnElCentro y/o tieneServicioEnElCurso.

## Parámetros específicos.

### Opción 1.
* **nifnie**: NIF o NIE del docente.
* **pasaporte**: Pasaporte del docente.

**Observaciones**: Debe cumplimentarse solamente uno de ellos.

### Opción 2.
* **tieneServicioEnElCentro**: Booleano que permite seleccionar a los docentes que tienen o han tenido algún servicio en el centro. Si no se indica, se seleccionan todos los docentes del centro.
* **tieneServicioEnElCurso**: Cuando se ha seleccionado la opción anterior, permite indicar el curso escolar en el que ha tenido servicio un docente (Ej. 2023).

**Observaciones**: Ambos son opcionales.

# Ejemplos.
### A) Solicitud de datos extendidos del docente con nif = 00000001R en el centro con código "35010488".
* ?opcion=1 & codigoCentro=35010488 & nifnie=00000001R & nivelDetalle=e

### B) Solicitud de datos reducidos de todos los docentes del centro con código "35010488".
* ?opcion=2 & codigoCentro=35010488

### C) Solicitud de datos con nivel de detalle medio de los docentes del centro con código "35010488" y servicio en el curso 2023. 
* ?opcion=2 & codigoCentro=35010488 & tieneServicioEnElCentro=true & tieneServicioEnElCurso=2023 & nivelDetalle=m


