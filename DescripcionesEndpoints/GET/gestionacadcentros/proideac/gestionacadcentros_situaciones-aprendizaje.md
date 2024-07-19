# Descripción general

Existen dos tipos de situaciones de aprendizaje:

* Públicas: Disponemos de dos catálogos de SSAA: El catálogo público y las situaciones de aprendizaje "brújula 20".
* Privadas: Pueden estar asociadas a un docente o a un nombramiento de un docente ( un servicio docente )

# Parámetros
Dispondremos de 4 paquetes de parametrización, uno por cada tipología de Situación de Aprendizaje.

## Parámetros comunes
### Parámetros:
Los parámetros comunes a todas las opciones son:
* **opcion.**
* **nivelDetalle.**
* **idEstudioSC** 
* **idAreaSC** 
* **tituloContiene** 


### Observaciones:
* El parámetro "opcion" es obligatorio y podrá tomar los valores: 1, 2, 3, 4. Cada valor se corresponde con un tipo de entidad.
> * Opción 1: Devolverá SSAA vinculadas a nombramiento de docentes (servicios docentes).
> * Opción 2: Devolverá SSAA vinculadas a docentes, directamente.
> * Opción 3: Devolverá SSAA del catálogo público.
> * Opción 4: Devolverá SSAA Brújula 20.

* El parámetro nivelDetalle podrá tomar los valores "r" (reducido), "m" (medio) y "e" (extendido). Cada valor devolverá una estructura diferente, siendo la opción "e" la que aporta mayor detalle y "r" la opción que oferta menor detalle.

* El parámetro "idEstudioSC" es opcional. Si se incluye, se filtrarán las SSAA relacionadas con, al menos, un área del estudio.
* El parámetro "idAreaSC" es opcional. Si se incluye, se filtrarán las SSAA relacionadas con, al menos, el área pasada como parámetro. Si se cumplimenta este parámetro no será necesario cumplimentar el parámetro "idEstudioSC". No obstante, hay que tener en cuenta que la devolución de SSAA podrá ser la colección vacía si se cumplimentan ambos parámetros y no son consistentes ( el área no se corresponde con el estudio )
* Es obligatorio pasar como parámetro el IdAreaSC o IdEstudioSC

* El parámetro "tituloContiene" no es obligatorio. Nos permitirá filtrar las SSAA cuyo título contenga la cadena pasada como parámetro.

## Parámetros específicos de la opción 1
El objetivo de los parámetros de la opción 1 es la identificación de un servicio docente ( nombramiento de un docente en un centro )

### Parámetros:
* **nifnieDocente** 
* **codigoCentro**
* **fechaReferenciaServicioDocente**  

### Observaciones:
* Los parámetros "nifnieDocente" y "codigoCentro" son obligatorios.
* El parámetro "fechaReferenciaServicioDocente" no es obligatorio. Si se omite se considerará la fecha del Sistema como fecha de referencia. Nótese que para garantizar unicidad de la identificación de un servicio es necesario una fecha de referencia puesto que un docente puede tener definidos múltiples servicios en un centro, siempre que no se solapen en el tiempo.

## Parámetros específicos de la opción 2
En este caso se devolverán las SSAA asociadas al docente con el nif/nie pasado como parámetro. Es importante destacar que solo se devuelven SSAA asociadas al docente. No se devolverán las SSAA asociadas a los nombramientos.

### Parámetros:
* **nifNieDocente**: 

### Observaciones:
* El parámetro "nifNieDocente" es obligatorio.

## Parámetros específicos de la opción 3
No contiene parámetros adicionales.

## Parámetros específicos de la opción 4
No contiene parámetros adicionales.


# Ejemplos.
## A) Solicitud de una situación de aprendizaje en un nombramiento (servicio docente)
Obtener las situaciones de aprendizaje vinculadas al servicio del docente con nif "12345678X" e el centro "38383838" y fecha de referencia "2022-12-03"
> * ?opcion=1 & nifnieDocente=12345678X & codigoCentro=38383838 and fechaReferenciaServicioDocente=2022-12-03

## B) Solicitud de SSAA Brújula 20.
Obtener las SSAA "Brújula 20" del área con identificador en SC "13245" y cuyo título contenga el texto "planeta" 
> * ?opcion=4 & idAreaSC=13245 & tituloContiene=planeta



