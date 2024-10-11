# Modificar 
# Modificar 
# Modificar 

# Descripción general.

Este endpoint proporciona todos los nombramientos docentes para un curso escolar o los de un determinado docente en un centro educativo según la opción y parámetros escogidos.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.

**Observaciones**:
* Opción 1: Además del *cursoEscolar*, es necesario indicar el *codigoCentro*.
* Opción 2: Solo debe cumplimentarse uno de los parámetros *nifNie* o *pasaporte*.

## Parámetros específicos.

### Opción 1.

* **cursoEscolar**: Obligatorio (Ej. 2022).
* **codigoCentro**: Obligatorio (Ej. 35009139).
* **fechaReferencia**: Devuelve solo los nombramientos vigentes en esa fecha (Ej. 2024-10-10). Si no se indica, suministra todos los nombramientos en el curso especificado.

### Opción 2.
* **nifNie**: Obligatorio si no se indica pasaporte.
* **pasaporte**: Obligatorio si no se indica nifNie.

**Observaciones**: El parámetro *fechaReferencia* no está permitido en esta opción.

# Ejemplos.
### A) Solicitud de todos los docentes con nombramiento vigente a fecha 01/12/2023 del centro con código "35010488" en el curso 2024.
* /gestionacadcentros/docentes-servicios?opcion=1 & cursoEscolar=2024 & codigoCentro=35010488 & fechaReferencia=2023-12-01

### B) Solicitud de todos los docentes con nombramiento en el curso 2022 del centro con código "35008381".
* /gestionacadcentros/docentes-servicios?opcion=1 & cursoEscolar=2022 & codigoCentro=35008381

### C) Solicitud de todos los nombramientos del docente con pasaporte "ABC000123".
* /gestionacadcentros/docentes-servicios?opcion=2 & pasaporte=ABC000123

### D) Solicitud de todos los nombramientos del docente con NIF "ABC000123".
* /gestionacadcentros/docentes-servicios?opcion=2 & nIFNIE=00000001R



