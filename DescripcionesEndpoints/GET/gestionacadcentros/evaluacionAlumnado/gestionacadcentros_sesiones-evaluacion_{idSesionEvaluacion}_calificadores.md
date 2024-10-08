
# Descripción general.

Este endpoint proporciona los calificadores de una sesión de evaluación (Ej. Bien, 9, No superada, etc.) a partir del parámetro *idSesionEvaluacion*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **idSesionEvaluacion**: Obligatorio (Ej. a03b12da48ae4bfd9ac9180c1aca1710)

**Observaciones**:
* Opción 1: El *idMatriculaArea* es obligatorio (Ej. 2C1A14915209497B99290AA13948DD86).
* Opción 2: El *idAreaSC* es obligatorio (Ej. 95450).

## Parámetros específicos.

### Opción 1.
* **idMatriculaArea**: Obligatorio (Ej. 2C1A14915209497B99290AA13948DD86).

**Observaciones**: El campo idAreaSC no produce ningún efecto en esta opción.

### Opción 2.
* **idAreaSC**: Obligatorio (Ej. 96563).

**Observaciones**: El campo idmatriculaArea no produce ningún efecto en esta opción.

# Ejemplos.
### A) Solicitud de datos de la sesión de evaluación con idSesionEvaluacion = "a03b12da48ae4bfd9ac9180c1aca1710".
* /gestionacadcentros/sesiones-evaluacion/a03b12da-48ae-4bfd-9ac9-180c1aca1710







# Ejemplos.
### A) Solicitud de todas las fotos del alumnado con pasaporte "119227796" del centro con código "35010488".
* /gestionacadcentros/alumnado/fotos?opcion=1 & codigoCentro=35010488 & pasaporte=119227796

### B) Solicitud de la foto más reciente del alumnado con idAlumnadoCentro = "EA1EF2E1E86B42F5A6591152F745EF37".
* /gestionacadcentros/alumnado/fotos?opcion=2 & idAlumnadoCentro=EA1EF2E1E86B42F5A6591152F745EF37
