# Descripción general.

Este endpoint proporciona datos de las matrículas asociadas a los responsables del alumnado.

## Parámetros específicos.

* **cursoEscolar**: Si se indica, muestra las matrículas para el curso escolar especificado (Ej. 2022).
* **codigoCentro**: Si se indica, muestra las matrículas para el centro especificado (Ej. 35010488).
* **nifNieResponsable**: NIF o NIE del responsable del alumnado.
* **pasaporteResponsable**: Pasaporte del responsable del alumnado.

**Observaciones**: Se debe escoger uno solo de los campos _nifNieResponsable_ o _pasaporteResponsable_.

# Ejemplos.
### A) Solicitud de datos de las matrículas asociadas al responsable con pasaporte = "INV234567" del centro con código "35010488".
* /gestionacadcentros/responsables-matriculas?codigoCentro=35010488 & pasaporteResponsable=INV234567
 
### B) Solicitud de datos de todas las matrículas asociadas al responsable con DNI = "41414141L".
* /gestionacadcentros/responsables-matriculas?nifNieResponsable=41414141L
  
