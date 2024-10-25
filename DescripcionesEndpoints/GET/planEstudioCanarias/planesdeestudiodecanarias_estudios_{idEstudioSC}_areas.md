# Descripción general.

Este endpoint proporciona la colección de áreas (Ej. *Ciencias de la Naturaleza*, *Análisis de la forma*, *Formación en Centros de Trabajo*, etc.) de un estudio concreto del Plan de Estudios de Canarias a partir del parámetro *idEstudioSC* para un determinado curso escolar.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2023).
* **idEstudioSC**: Obligatorio (Ej. 7357).
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

# Ejemplos.
### A) Solicitud de las áreas con nivelDetalle *medio* del estudio con idEstudioSC = "9043" para el curso 2024.
* /planesdeestudiodecanarias/estudios/9043/areas?cursoEscolar=2024 & nivelDetalle=m

### B) Solicitud de las áreas con nivelDetalle *reducido* del estudio con idEstudioSC = "6546" para el curso 2023.
* /planesdeestudiodecanarias/estudios/6546/areas?cursoEscolar=2023
