# Descripción general.

Este endpoint devuelve las evaluaciones de un centro educativo.

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **idEnsenyanza**: Si no se indica, se muestran las evaluaciones de todas las enseñanzas.

**Observaciones**:
* Opción 1: Los campos obligatorios son el *cursoEscolar* y el *codigoCentro*.
* Opción 2: El campo *idCursoCentro* es obligatorio.

## Parámetros específicos.

### Opción 1.
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773).
* **idCursoCentro**: Si no se indica, se muestran todas las evaluaciones para el curso y centro especificado (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idEnsenyanza**: Si no se indica, se muestran las evaluaciones de todas las enseñanzas del curso y centro especificado (Ej. FF31EB108792412187C73076537F5822).

**Observaciones**: El campo *idCursoCentro* no se tienen en cuenta en esta opción, ya que queda determinado por los campos *cursoEscolar* y *codigoCentro*.

### Opción 2.
* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).
* **idEnsenyanza**: Si no se indica, se muestran todas las evaluaciones para el idCursoCentro introducido.

**Observaciones**: Los campos *cursoEscolar* y *codigoCentro* están permitidos en esta opción, pero no se tienen en cuenta ya que quedan determinados por el campo *idCursoCentro*.

# Ejemplos.
### A) Solicitud de las evaluaciones del curso 2019 para la enseñanza con idEnsenyanza = "C3E9383D03D94CD183CE15DAF8BF3E1D" del centro con código "35010488".
* /gestionacadcentros/evaluaciones?opcion=1 & cursoEscolar=2019 & codigoCentro=35010488 & idEnsenyanza=C3E9383D03D94CD183CE15DAF8BF3E1D

### B) Solicitud de todas las evaluaciones para el idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/evaluaciones?opcion=2 & idCursoCentro=E480D237EC8C4AFFA87001C277A3D712

### C) Solicitud de las evaluaciones de la enseñanza con idEnsenyanza = "FF31EB108792412187C73076537F5822" e idCursoCentro = "E480D237EC8C4AFFA87001C277A3D712".
* /gestionacadcentros/evaluaciones?opcion=2 & idCursoCentro=E480D237EC8C4AFFA87001C277A3D712 & idEnsenyanza=FF31EB108792412187C73076537F5822
