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

**Observaciones**:
* El endpoint **solo atenderá la petición si el remitente o destinatario** pasado como parámetro en la llamada **corresponde al usuario autenticado**. En caso contrario, se dará la respuesta establecida para la no autorización de la llamada.
* Ninguno de los campos *nifNieRemitente*, *pasaporteRemitente* o *cialRemitente* es obligatorio, pero si se especifica, solo se podrá indicar uno de ellos.
* Ninguno de los campos *nifNieDestinatario*, *pasaporteDestinatario* o *cialDestinatario* es obligatorio, pero si se especifica, solo se podrá indicar uno de ellos.
* En las llamadas se deberá incluir al menos un parámetro que identifique al remitente o al destinatario.

# Ejemplos.
### A) Solicitud de datos de todas las comunicaciones en web del remitente con nifNieRemitente = "41414141L".
* /gestionacadcentros/envios-comunicaciones-en-web?nifnieRemitente=41414141L
 
### B) Solicitud de datos de todas las comunicaciones en web entre el remitente con DNI = "41414141L" y el destinatario con CIAL = "60000000S" entre los días 01/05/2024 y 30/06/2024.
* /gestionacadcentros/envios-comunicaciones-en-web?nifnieRemitente=41414141L & cialDestinatario=60000000S & fechaDesde=2024-05-01 & fechaHasta=2024-06-30

### C) Solicitud de datos de las últimas 5 comunicaciones en web recibidas por el destinatario con nifNieDestinatario = "41414141L".
* /gestionacadcentros/envios-comunicaciones-en-web?nifnieDestinatario=41414141L & ultimas=5

### D) Solicitud de datos de la última comunicación en web entre el remitente con DNI = "41414141L" y el destinatario con DNI = "60000000S" entre los días 01/09/2023 y 22/12/2023.
* /gestionacadcentros/envios-comunicaciones-en-web?nifnieRemitente=41414141L & nifnieDestinatario=60000000S & fechaDesde=2023-09-01 & fechaHasta=2023-12-22 & ultimas=1

  
