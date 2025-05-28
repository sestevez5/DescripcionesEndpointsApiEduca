
# Descripción general.

Este endpoint proporciona la colección de áreas (Ej. *Ciencias de la Naturaleza*, *Análisis de la forma*, *Formación en Centros de Trabajo*, etc.) de las diferentes enseñanzas y estudios del Plan de Estudios de Canarias para un determinado curso escolar.

## Parámetros específicos.

* **cursoEscolar**: Obligatorio (Ej. 2023).
* **idEnsenyanzaSC**: Obligatorio si no se indica *idEstudioSC* (Ej. 103).
* **idEstudioSC**: Obligatorio si no se indica *idEnsenyanzaSC* (Ej. 7357).
* **incluirNoVigentes**: Si se selecciona, incluye las áreas de los estudios no vigentes. Si se escoge "No" o "No establecido", devuelve solo las de los estudios vigentes.
* **nivelDetalle**: r, m (reducido, medio). Si no se indica, su valor por defecto será r.

**Observaciones**: Los campos *idEnsenyanzaSC* e *idEstudioSC* no son obligatorios, pero hay que especificar al menos uno de ellos.

# Ejemplos.
### A) Solicitud de las áreas con nivelDetalle *medio* para los estudios vigentes con idEstudioSC = "7357" de la enseñanza con idEnsenyanzaSC = "103" para el curso 2024.
* /planesdeestudiodecanarias/areas?cursoEscolar=2024 & idEnsenyanzaSC=103 & idEstudioSC=7357 & nivelDetalle=m

### B) Solicitud de las áreas con nivelDetalle *reducido* para los estudios, incluidos los no vigentes, de la enseñanza con idEnsenyanzaSC = "110" para el curso 2023.
* /planesdeestudiodecanarias/areas?cursoEscolar=2023 & idEnsenyanzaSC=110 & incluirNoVigentes=true

### C) Solicitud de las áreas con nivelDetalle *reducido* para los estudios vigentes con idEstudioSC = "7555" para el curso 2022. 
* /planesdeestudiodecanarias/areas?cursoEscolar=2022 & idEstudioSC=7555 & incluirNoVigentes=false & nivelDetalle=r
