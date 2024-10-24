# Descripción general.

Este endpoint devuelve las diferentes enseñanzas (Ej. *Educación Primaria*, *Ciclos Formativos de Grado Básico*, *Bachillerato*, etc.) que figuran en el Plan de Estudios de Canarias para un determinado curso escolar.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2024).
* **incluirNoVigentes**: Si se selecciona, incluye las enseñanzas no vigentes. Si se escoge "No" o "No establecido", devuelve solo las enseñanzas vigentes.

# Ejemplos.
### A) Solicitud de todas las enseñanzas vigentes en el curso 2024.
* /planesdeestudiodecanarias/ensenyanzas?cursoEscolar=2024

### B) Solicitud de todas las enseñanzas, incluidas las no vigentes, en el curso 2021.
* /planesdeestudiodecanarias/ensenyanzas?cursoEscolar=2021 & incluirNovigentes=true
