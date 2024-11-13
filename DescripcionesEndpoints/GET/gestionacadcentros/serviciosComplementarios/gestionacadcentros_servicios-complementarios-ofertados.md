# MODIFICAR
# MODIFICAR
# MODIFICAR

# Descripción general.

Este endpoint proporciona los servicios complementarios ofertados por un centro educativo concreto en un curso escolar determinado.

## Parámetros comunes.
* **codigoCentro**: Obligatorio (Ej. 38010773)
* **idCursoEscolar**: Obligatorio (Ej. 2022)
* **codTipoServicioComplementario**: Opcional. Si no se indica, se muestran todos los servicios complementarios.
* **idTipoServicioComplementario**: Opcional. Si no se indica, se muestran todos los servicios complementarios.


**Observaciones**:
* Solo se puede indicar uno de los parámetros opcionales.

# Ejemplos.
### A) Solicitud de datos del centro con código "38011108".
* /gestionacadcentros/centros?codigoCentro=38011108

### B) Solicitud de los centros públicos de la isla de Tenerife.
* /gestionacadcentros/centros?isla=7 & naturaleza=1

### C) Solicitud de los centros de la zona de inspección 401 en el curso 2021. 
* /gestionacadcentros/centros?zonaInspeccion=401 & cursoEscolarZonaInspeccion=2021
