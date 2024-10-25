
# Descripción general.

Este endpoint devuelve las evaluaciones definidas en el Plan de Estudio de Canarias para un determinado curso escolar.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2023).
* **idEnsenyanzaSC**: Si no se indica, se muestran las evaluaciones de todas las enseñanzas del curso escolar especificado.

# Ejemplos.
### A) Solicitud de las evaluaciones del curso 2024 para la enseñanza con idEnsenyanzaSC = "2".
* /planesdeestudiodecanarias/evaluaciones?cursoEscolar=2024 & idEnsenyanzaSC=2

### B) Solicitud de todas las evaluaciones para el curso 2023.
* /planesdeestudiodecanarias/evaluaciones?cursoEscolar=2023

