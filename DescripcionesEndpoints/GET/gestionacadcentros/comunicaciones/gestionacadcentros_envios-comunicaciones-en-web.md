# Descripción general.

Este endpoint proporciona datos relativos al envío de comunicaciones en web de Pincel Ekade.

## Parámetros específicos.

* **nifNieRemitente**: NIF o NIE del remitente de la comunicación.
* **pasaporteRemitente**: Pasaporte del remitente de la comunicación.
* **cialRemitente**: CIAL del remitente de la comunicación.
* **nifNieDestinatario**: NIF o NIE del destinatario de la comunicación.
* **pasaporteDestinatario**: Pasaporte del destinatario de la comunicación.
* **cialDestinatario**: CIAL del destinatario de la comunicación.
* **fechaDesde**: Si se indica, devuelve todos los envíos de comunicaciones en web cuya fecha de envío sea igual o posterior al valor del parámetro _fechaDesde_.
* **fechahasta**: Si se indica, devuelve todos los envíos de comunicaciones en web cuya fecha de envío sea igual o anterior al valor del parámetro _fechaHasta_.
* **ultimas**: Si se indica, devuelve el número especificado de comunicaciones en web más recientes.

**Observaciones**: Se debe escoger uno solo de los campos _nifNieResponsable_ o _pasaporteResponsable_.

# Ejemplos.
### A) Solicitud de datos de las matrículas asociadas al responsable con pasaporte = "INV234567" del centro con código "35010488".
* ?codigoCentro=35010488 & pasaporteResponsable=INV234567
 
### B) Solicitud de datos de todas las matrículas asociadas al responsable con DNI = "41414141L".
* ?nifNieResponsable=41414141L
  
