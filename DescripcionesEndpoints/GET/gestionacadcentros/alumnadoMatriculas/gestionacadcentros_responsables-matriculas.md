# Descripción general

Este endpoint proporciona datos de las matrículas asociadas a los responsables del alumnado.

## Parámetros específicos

* **cursoEscolar**:
* **codigoCentro**:
* **nifNieResponsable**: NIF o NIE del responsable del alumnado.
* **pasaporteResponsable**: Pasaporte del responsable del alumnado.

**Observaciones**: Se debe escoger uno solo de los campos _nifNieResponsable_ o _pasaporteResponsable_.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle medio del responsable con dni = "12345678Z" del centro con código "35010488".
* ?opcion=1 & codigoCentro=35010488 & nifNie=12345678Z & nivelDetalle=m
 
### B) Solicitud de datos con nivelDetalle extendido de todos  los responsables del centro con código "35010488".
* ?opcion=2 & codigoCentro=35010488 & nivelDetalle=e

### C) Solicitud de datos con nivelDetalle reducido de los responsables con alumnado tutelado que esté matriculado en el curso 2022 en el centro con código "35010488". 
* ?opcion=2 & codigoCentro=35010488 & tieneTuteladoMatriculaEnElCentro=true & tieneTuteladoMatriculaEnElCurso=2022
