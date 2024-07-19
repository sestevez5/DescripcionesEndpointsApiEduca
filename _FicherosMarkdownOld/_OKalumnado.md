# Descripción general

Este endpoint está dirigido a ofrecer información del alumnado registrado en los distintos centros educativos:

# Parámetros
Dispondremos de tres paquetes de parametrización.

## Parámetros comunes
### Parámetros:
Los parámetros comunes a todas las opciones son:
* **opcion**  (obligatorio)
* **nivelDetalle** 
* **tieneMatriculaEnElCentro** (booleano no obligatorio, false por defecto)
* **conMatriculaEnElCurso** (entero no obligatorio. Ej.: 2022, 2023,...)
* **tieneMatriculaActiva** (booleano no obligatorio, false por defecto)
* **codigoCentro** (opcional, por defecto. Ej.: 38102345 )


### Observaciones:
* El parámetro "opcion" es obligatorio y podrá tomar los valores: 1, 2, 3.
> * Opción 1: Devolverá el alumnado de un centro educativo.
> * Opción 2: Devolverá el alumnado identificado a partir de un documento identificativo.
> * Opción 3: Devolverá el alumnado tutelado por un responsable identificado a partir de un documento identificativo.

* El parámetro "nivelDetalle" nos habilita la posibilidad de elgir la cantidad de información a obtener: r (reducido), m (medio), e (extendido). El valor por defecto es r

## Parámetros específicos de la opción 1
Se trata de una opción que no incluye parámetros específicos, aunque obliga a definir el parámetro común "codigoCentro" que, por defecto, no tiene carácter obligatorio.

## Parámetros específicos de la opción 2
Esta opción nos ofrece la posibilidad de obtener todos los registros de alumnado en los distintos centros educativos a partir de un documento identificativo de un alumno/a.

### Parámetros:
* **nifNieAlumnado**: 
* **cialAlumnado**: 
* **pasaporteAlumnado**: 

### Observaciones:
* Ninguno de los tres parámetros es obligatorio, pero debe cumplimentarse, al menos, uno.

## Parámetros específicos de la opción 3
Esta opción nos ofrece la posibilidad de obtener todos los registros de alumnado tutelado por un responsable identificado como parámetro.

### Parámetros:
* **nifNieResponsable**
* **pasaporteResponsable**

### Observaciones:
* Niguno de los parámetros es obligatorio pero debe cumplimentarse, al menos, uno.


# Ejemplos.

A) Solicitud de los registros de alumnado que no tengan matricula activa tutelado por el responsable con nifnie "12345678X"
> * ?opcion=3 & nifNieResponsable=12345678X & tieneMatriculaActiva=false 



** Notas: 

1) Solo se devolverán las relacienes tutelado-responsables cuando el responsable tenga derecho a información.
2) Una matrícula activa es una matrícula sin fecha de finalización correspondiente al curso escolar que contenga la fecha del sistema en su periodo administrativo.

