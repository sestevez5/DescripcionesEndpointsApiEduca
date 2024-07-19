# Descripción general

En el sistema educativo LOMLOE se han establecido un conjunto de "saberes básicos" por cada una de las áreas de las enseñanzas obligatorias. En este endpoint dispondemos de distintas opciones de parametrización para la obtención de esta información 

# Parámetros:
Dispondremos de distintos paquetes de parametrización. A continuación se describen los parámetros query:

## Parámetros comunes:
* **opcion.**. Es un parámetro obligatorio que podrá tomar los valores 1, 2, 3.
* **nivelDetalle.** (obligatorio)
 El parámetro nivelDetalle podrá tomar los valores "r" (reducido), "m" (medio) y "e" (extendido). Cada valor devolverá una estructura diferente, siendo la opción "r" la que aporta menor detalle y "e" la opción más rica. 


## Parámetros específicos de opción:
* IdAreaSC: es un parémtro obligatorio y solo permitido en la opción 1. Con este parámetro se devolverá la colección de saberes básicos correspondientes al área indicada como parámetro.  
* idEstudioSC: es un parémtro obligatorio y solo permitido en la opción 2. Con este parámetro se devolverá la colección de saberes básicos correspondientes a las áreas del estudio indicado como parámetro.  
* idEnsenyanzaSC: es un parémtro obligatorio y solo permitido en la opción 3. Con este parámetro se devolverá la colección de saberes básicos correspondientes a las áreas de la enseñanza indicada como parámetro. 




