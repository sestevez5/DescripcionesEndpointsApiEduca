# Descripción general

Este endpoint proporciona los datos personales de los responsables del alumnado de un centro a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

## Parámetros específicos

* **idCentro**: Obligatorio (Ej. 561EBA45-51E5-4E3F-BA6B-C4CBB8363079)
* **tieneTuteladoMatriculaEnElCentro**: permite seleccionar a los responsables del alumnado que tiene matrícula.
  * No establecido: Devuelve todos los responsables del alumnado del centro.
  * Sí: Devuelve a los responsables del alumnado con matrícula en el centro.
  * No: Devuelve a los responsables del alumnado que no tiene matrícula en el centro.
* **tieneTuteladoMatriculaEnElCurso**: selecciona a los responsables del alumnado que tiene matrícula en el curso escolar indicado (Ej. 2023). 

# Ejemplos.
### A) Solicitud de datos extendidos de todos los responsables del alumnado en un centro para un idCentro concreto.
* 561EBA45-51E5-4E3F-BA6B-C4CBB8363079/responsables?nivelDetalle=e
   
### **B**) Solicitud de datos medios de los responsables del alumnado con matrícula en el curso 2024 para un idCentro concreto.
* 561EBA45-51E5-4E3F-BA6B-C4CBB8363079/responsables?tieneTuteladoMatriculaEnElCentro=true & tieneTuteladoMatriculaEnElCurso=2024 & nivelDetalle=m
