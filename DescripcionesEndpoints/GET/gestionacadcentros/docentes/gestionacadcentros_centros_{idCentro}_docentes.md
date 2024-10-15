# Descripción general.

Este endpoint devuelve los datos de los docentes de un centro educativo a partir del parámetro _idCentro_, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros comunes.
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.

## Parámetros específicos.

* **idCentro**: Obligatorio (Ej. 561EBA4551E54E3FBA6BC4CBB8363079)
* **tieneServicioEnElCentro**: Booleano que permite seleccionar a los docentes que tienen o han tenido algún servicio en el centro. Si no se indica, se seleccionan todos los docentes del centro.
* **tieneServicioEnElCurso**: Cuando se ha seleccionado la opción anterior, permite indicar el curso escolar en el que ha tenido servicio un docente (Ej. 2023).

**Observaciones**:
* Si se escoge el valor "No" en el campo _tieneServicioEnElCentro_, no es posible especificar el campo _tieneServicioEnElCurso_, devolviéndose un mensaje de error en este caso.

# Ejemplos.
### A) Solicitud de datos con nivelDetalle *reducido* de todos los docentes del centro con idCentro = "561EBA4551E54E3FBA6BC4CBB8363079".
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/docentes

### B) Solicitud de datos con nivelDetalle *medio* de los docentes con servicio en el curso 2024 para el idCentro = "561EBA4551E54E3FBA6BC4CBB8363079".
* /gestionacadcentros/centros/561EBA4551E54E3FBA6BC4CBB8363079/docentes?tieneServicioEnElCentro=true & tieneServicioEnElCurso=2024 & nivelDetalle=m


