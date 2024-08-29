# Descripción general

Este endpoint proporciona información de los centros educativos.

## Parámetros comunes
* **codigoCentro**: Si no se indica, se muestran todos los centros (Ej. 38010773)
* **idCentroSC**: Si no se indica, se muestran todos los centros (Ej. 2250)
* **codEtapaCentro**: Si no se indica, se muestran todos los tipos de centros (Ej. IES).
* **isla**: Si no se indica, se muestran los centros de todas las islas (Ej. 3, muestra los centros de Gran Canaria).
* **naturaleza**: Si no se indica, se muestran los centros de cualquier naturaleza (Ej. 1, ofrece los centros públicos).
* **zonaInspeccion**: Si no se indica, se muestran los centros de todas las zonas de inspección (Ej. 305, ofrece los centros adscritos a esa zona).
* **cursoEscolarZonaInspeccion**: Si no se indica, se muestran los centros para todos los cursos (Ej. 2022, ofrece los centros de ese curso).
* **codigoMunicipio**: Si no se indica, se muestran los centros de todos los municipio (Ej. 38005, ofrece los centros con ese código)

**Observaciones**:
* Todos los parámetros son opcionales.

# Ejemplos.
### A) Solicitud de datos del centro con código "38011108".
* ?codigoCentro=38011108

### B) Solicitud de los centros públicos de la isla de Tenerife.
* ?isla=7 & naturaleza=1

### C) Solicitud de los centros de la zona de inspección 401 en el curso 2021. 
* ?zonaInspeccion=401 & cursoEscolarZonaInspeccion=2021
