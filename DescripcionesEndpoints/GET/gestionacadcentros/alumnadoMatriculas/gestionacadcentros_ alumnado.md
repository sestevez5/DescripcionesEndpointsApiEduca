# Descripción general

Este endpoint proporciona datos personales del alumnado registrado en los centros educativos así como de sus responsables.

## Parámetros comunes

* **opcion**: 1, 2, 3. Se deberá escoger uno obligatoriamente.
* **tieneMatriculaEnElCentro**: selecciona al alumnado que está matriculado al menos en un curso escolar.
* **conMatriculaEnElCurso**: selecciona al alumnado que está matriculado en el curso escolar indicado (Ej. 2024).
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.
* **tieneMatriculaActiva**: selecciona al alumnado con matrícula sin fecha de finalización en el curso escolar indicado.

**Observaciones**:
>* Opción 1: Devuelve los datos personales de todo el alumnado a partir del codigoCentro (obligatorio).
>* Opción 2: Devuelve los datos personales del alumnado a partir de su cial, nifnie o pasaporte, siendo obligatorio uno solo de los mismos.
>* Opción 3: Devuelve los datos del alumnado tutelado y de sus responsables a partir del nifnie o pasaporte del responsable, siempre que tenga derecho a información.

## Parámetros específicos

### Opción 1
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: Los campos cial, nifNie, pasaporte, nifNieResponsable y pasaporteResponsable no están permitidos en esta opción.

### Opción 2
* **cial**: CIAL del alumnado.
* **nifnie**: NIF o NIE del alumnado.
* **pasaporte**: Pasaporte del alumnado.

**Observaciones**: Sólo se debe proporcionar uno de los datos identificativos del alumnado (cial, nifNie o pasaporte). Los campos nifNieResponsable y pasaporteResponsable no están permitidos en esta opción.

### Opción 3
* **nifNieResponsable**: NIF o NIE del responsable del alumnado.
* **pasaporteResponsable**: Pasaporte del responsable del alumnado.

**Observaciones**: Sólo es necesario indicar uno de los datos identificativos del responsable. Los campos cial, nifNie y pasaporte no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle extendido del alumno con cial B00P08015J.
* ?opcion=2 & cial=B00P08015J & nivelDetalle=e

### B) Solicitud de datos con nivelDetalle reducido de todo el alumnado del centro con código "35010488".
* ?opcion=1 & codigoCentro=35010488

### C) Solicitud de datos con nivelDetalle medio del alumnado del centro con código "35010488" y matrícula en el curso 2023.
* ?opcion=1 & codigoCentro=35010488 & conMatriculaEnElCurso=2023 & nivelDetalle=m

### D) Solicitud de datos con nivelDetalle extendido del alumnado tutelado por el responsable con pasaporte "DWM669980P".
* ?opcion=3 & tieneMatriculaActiva=true & pasaporteResponsable=DWM669980P & nivelDetalle=e

