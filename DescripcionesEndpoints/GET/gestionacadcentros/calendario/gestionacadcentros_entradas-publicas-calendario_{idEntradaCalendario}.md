# Descripción general.

Este endpoint devuelve la colección de entradas públicas del calendario, es decir, aquellas que son visibles para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*) a partir del parámetro *idEntradaCalendario*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idEntradaCalendario**: Obligatorio (Ej. 8A3C8338-C34D-431F-AB68-0000A69092B4)

# Ejemplos.
### A) Solicitud de entradas públicas del curso escolar actual para el centro con código "35009139".
* ?opcion=1 & codigoCentro=35009139

### B) Solicitud de entradas públicas del centro con idCentro = "561EBA45-51E5-4E3F-BA6B-C4CBB8363079" desde el día 01/06/2022.
* ?opcion=2 & idCentro=561EBA45-51E5-4E3F-BA6B-C4CBB8363079 & fechaDesde=2022-06-01

### C) Solicitud de entradas públicas del centro con código "35010488" desde el 01/01/2020 hasta el 05/09/2024.
* ?opcion=1 & codigoCentro=35010488 & fechaDesde=2020-01-01 & fechaHasta=2024-09-05
