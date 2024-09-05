# Descripción general.

Este endpoint devuelve la colección de entradas públicas del calendario, es decir, aquellas que son visibles para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*).

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **fechaDesde**: Si se indica, devuelve las entradas con fecha igual o posterior a la especificada (Ej. 2023-05-01T09:30:00).
* **fechaHasta**: Si se indica, devuelve las entradas con fecha igual o anterior a la especificada (Ej. 2023-03-15T14:00:00).

**Observaciones**:
* En el caso de no establecerse los parámetros fechaDesde o fechaHasta, se utilizarán los del periodo administrativo del curso escolar actual a fecha del sistema.
* Opción 1: Devuelve las entradas públicas a partir del codigoCentro (obligatorio).
* Opción 2: Devuelve las entradas públicas a partir del idCentro (obligatorio).

## Parámetros específicos.

### Opción 1.
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: El parámetro idCentro no está permitido en esta opción.

### Opción 2.
* **idCentro**: Obligatorio (Ej. 7C6F1441-12B7-4D59-96AA-55AD4BE7662F).

**Observaciones**: El parámetro codigoCentro no está permitidos en esta opción.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle extendido del alumno con cial B00P08015J.
* ?opcion=2 & cial=B00P08015J & nivelDetalle=e

### B) Solicitud de datos con nivelDetalle reducido de todo el alumnado del centro con código "35010488".
* ?opcion=1 & codigoCentro=35010488

### C) Solicitud de datos con nivelDetalle medio del alumnado del centro con código "35010488" y matrícula en el curso 2023.
* ?opcion=1 & codigoCentro=35010488 & conMatriculaEnElCurso=2023 & nivelDetalle=m

### D) Solicitud de datos con nivelDetalle extendido del alumnado tutelado por el responsable con pasaporte "DWM669980P".
* ?opcion=3 & tieneMatriculaActiva=true & pasaporteResponsable=DWM669980P & nivelDetalle=e

