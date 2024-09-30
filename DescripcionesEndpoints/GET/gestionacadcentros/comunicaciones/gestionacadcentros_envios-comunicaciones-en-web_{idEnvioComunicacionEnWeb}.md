# Descripción general.

Este endpoint proporciona datos detallados relativos al envío de comunicaciones en web de Pincel Ekade a partir del parámetro *idEnvioComunicacionEnWeb*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idEnvioComunicacionEnWeb**: Obligatorio (Ej. b9d83ae62bf344b4a1b3070bafec92ab)

**Observaciones**:

* El endpoint **solo atenderá la petición si el usuario autenticado es remitente o destinatario** del envío de la comunicación correspondiente al *IdEnvioComunicacionEnWeb* especificado.

# Ejemplo.
### A) Solicitud de datos de la comunicación en web con idEnvioComunicacionEnWeb = "36d7165f6ae64ac28875942d893e82d7".
* /gestionacadcentros/envios-comunicaciones-en-web/36d7165f6ae64ac28875942d893e82d7
 
