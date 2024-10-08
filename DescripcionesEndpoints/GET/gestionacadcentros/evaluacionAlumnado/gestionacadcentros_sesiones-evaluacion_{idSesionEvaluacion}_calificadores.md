
# Descripción general.

Este endpoint proporciona los calificadores de las matrículas-áreas de una sesión de evaluación (Ej. Bien, 9, No superada, etc.) a partir del parámetro *idSesionEvaluacion*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **idSesionEvaluacion**: Obligatorio (Ej. a03b12da48ae4bfd9ac9180c1aca1710)

**Observaciones**:
* Opción 1: El *idMatriculaArea* es obligatorio (Ej. 2C1A14915209497B99290AA13948DD86).
* Opción 2: El *idAreaSC* es obligatorio (Ej. 95450).

## Parámetros específicos.

### Opción 1.
* **idMatriculaArea**: Obligatorio (Ej. 2C1A14915209497B99290AA13948DD86).

**Observaciones**: El campo *idAreaSC* no produce ningún efecto en esta opción.

### Opción 2.
* **idAreaSC**: Obligatorio (Ej. 96563).

**Observaciones**: El campo *idMatriculaArea* no produce ningún efecto en esta opción.

# Ejemplos.
### A) Solicitud de los calificadores de la sesión de evaluación con idSesionEvaluacion = "a03b12da48ae4bfd9ac9180c1aca1710" e idMatriculaArea = 'C5E14D26C27D44AA869995DDE1D4419A'.
* /gestionacadcentros/sesiones-evaluacion/A03B12DA48AE4BFD9AC9180C1ACA1710/calificadores?opcion=1 & idMatriculaArea=C5E14D26C27D44AA869995DDE1D4419A

### B) Solicitud de los calificadores de la sesión de evaluación con idSesionEvaluacion = "a03b12da48ae4bfd9ac9180c1aca1710" e idAreaSC = "96563".
* /gestionacadcentros/sesiones-evaluacion/A03B12DA48AE4BFD9AC9180C1ACA1710/calificadores?opcion=2 & idAreaSC=96563
