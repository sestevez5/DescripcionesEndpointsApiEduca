# Descripción general.

Este endpoint proporciona los servicios complementarios ofertados por un centro educativo concreto en un curso escolar determinado.

## Parámetros comunes.
* **codigoCentro**: Obligatorio (Ej. 38010773)
* **idCursoEscolar**: Obligatorio (Ej. 2022)
* **codTipoServicioComplementario**: Opcional. Si no se indica, se muestran todos los servicios complementarios ofertados (Ej. 03).
* **idTipoServicioComplementario**: Opcional. Si no se indica, se muestran todos los servicios complementarios ofertados (Ej. 4).


**Observaciones**:
* Solo se puede indicar uno de los parámetros opcionales.

# Ejemplos.
### A) Solicitud de todos los servicios complementarios ofertados por el centro con código "35010488" en el curso escolar 2023.
* /gestionacadcentros/servicios-complementarios-ofertados?codCentro=35010488 & idCursoEscolar=2023

### B) Solicitud de información del servicio complementario con codigoTipoServicioComplementario = "02" del centro con código "35010488" en el curso escolar 2022.
* /gestionacadcentros/servicios-complementarios-ofertados?codCentro=35010488 & idCursoEscolar=2022 & codigoTipoServicioComplementario=02

### C) Solicitud de información del servicio complementario con idTipoServicioComplementario = "3" del centro con código "35010488" en el curso escolar 2024. 
* /gestionacadcentros/servicios-complementarios-ofertados?codCentro=35010488 & idCursoEscolar=2024 & idTipoServicioComplementario=3
