# Descripción general.

Este endpoint proporciona información de un centro educativo a partir del parámetro *idCentro*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idCentroSC**: Si no se indica, se muestran todos los centros (Ej. 2250)


**Observaciones**:
* Todos los parámetros son opcionales.

# Ejemplos.
### A) Solicitud de datos del centro con código "38011108".
* ?codigoCentro=38011108

### B) Solicitud de los centros públicos de la isla de Tenerife.
* ?isla=7 & naturaleza=1

### C) Solicitud de los centros de la zona de inspección 401 en el curso 2021. 
* ?zonaInspeccion=401 & cursoEscolarZonaInspeccion=2021
