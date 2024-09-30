# Descripción general.

Este endpoint devuelve las enseñanzas impartidas en los centros educativos (Ej. *Educación Primaria*, *Ciclos Formativos de Grado Básico*, *Bachillerato*, etc.).

## Parámetros comunes.
* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **incluirNoVigentes**: Si se selecciona, incluye las enseñanzas no vigentes. Si se escoge "No" o "No establecido", devuelve solo las enseñanzas vigentes.

**Observaciones**:
* Opción 1: Los campos obligatorios son el cursoEscolar y el codigoCentro.
* Opción 2: El campo idCursoCentro es obligatorio.

## Parámetros específicos.

### Opción 1.
* **cursoEscolar**: Obligatorio (Ej. 2023).
* **codigoCentro**: Obligatorio (Ej. 38010773).

**Observaciones**: El campo idCursoCentro no está permitido en esta opción.

### Opción 2.
* **idCursoCentro**: Obligatorio (Ej. E480D237EC8C4AFFA87001C277A3D712).

**Observaciones**: Los campos cursoEscolar y codigoCentro no están permitidos en esta opción.

# Ejemplos.
### A) Solicitud de todas las enseñanzas para el idCursoCentro especificado.
* /gestionacadcentros/ensenyanzas?opcion=2 & idCursoCentro=E480D237EC8C4AFFA87001C277A3D712

### B) Solicitud de todas las enseñanzas del centro con código "35007374" en el curso 2024.
* /gestionacadcentros/ensenyanzas?opcion=1 & cursoEscolar=2024 & codigoCentro=35007374

