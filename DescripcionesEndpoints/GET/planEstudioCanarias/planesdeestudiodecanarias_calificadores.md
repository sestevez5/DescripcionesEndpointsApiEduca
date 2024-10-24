
# Descripción general.

Este endpoint proporciona la colección de calificadores (Ej. Bien, 9, No superada, etc.) definidos para las enseñanzas vigentes que figuran en el Plan de Estudios de Canarias en un determinado curso escolar. 

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2024).
* **idEnsenyanzaSC**: Opcional (Ej. 110). Si no se indica, se devolverán los calificadores de todas las enseñanzas vigentes para el curso escolar especificado .

# Ejemplos.

### A) Solicitud de los calificadores de la enseñanza con idEnsenyanzaSC = "120" para el curso 2024.
* /planesdeestudiodecanarias/calificadores?cursoEscolar=2024 & idEnsenyanzaSC=120

### B) Solicitud de todos los calificadores de las enseñanzas vigentes en el curso 2023.
* /planesdeestudiodecanarias/calificadores?cursoEscolar=2023
