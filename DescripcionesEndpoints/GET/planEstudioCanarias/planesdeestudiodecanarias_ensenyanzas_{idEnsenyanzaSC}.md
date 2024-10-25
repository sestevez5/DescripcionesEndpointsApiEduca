
# Descripción general.

Este endpoint devuelve información de los estudios de una enseñanza concreta (Ej. *Educación Primaria*, *Ciclos Formativos de Grado Básico*, *Bachillerato*, etc.) del Plan de Estudios de Canarias  para un determinado curso escolar.

## Parámetros específicos.

* **idEnsenyanzaSC**: Obligatorio (Ej. 110)
* **cursoEscolar**: Obligatorio (Ej. 2024).
* **incluirNovigentes**: Si se selecciona, incluye los estudios no vigentes de la enseñanza especificada. Si se escoge "No" o "No establecido", devuelve solo los vigentes.

# Ejemplos.
### A) Solicitud de información de los estudios vigentes de la enseñanza con idEnsenyanzaSC = "129" en el curso 2024.
* /planesdeestudiodecanarias/ensenyanzas/129?cursoEscolar=2024

### B) Solicitud de información de los estudios, incluidos los no vigentes, de la enseñanza con idEnsenyanzaSC = "115" en el curso 2022.
* /planesdeestudiodecanarias/ensenyanzas/115?cursoEscolar=2022 & incluirNoVigentes=true
