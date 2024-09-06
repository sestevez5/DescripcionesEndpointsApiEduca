# Descripción general.

Este endpoint devuelve la colección de entradas públicas del calendario de un centro, es decir, aquellas que son visibles para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*).

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38010773)
* **fechaDesde**: Si se indica, devuelve las entradas con fecha igual o posterior a la especificada (Ej. 2023-05-01).
* **fechaHasta**: Si se indica, devuelve las entradas con fecha igual o anterior a la especificada (Ej. 2023-03-15).
* **tipoEntrada**: Si se indica, se devuelven solamente las entradas cuyo código coincida con el especificado, y que corresponden al parámetro _codigo_ de la tabla XCA_TTipoEntradaCalendario (Ej. FES devuelve los días festivos).

**Observaciones**:
* En el caso de no establecerse los parámetros fechaDesde y fechaHasta, se devolverán todas las entradas públicas del calendario.

# Ejemplos.
### A) Solicitud de entradas públicas del curso escolar actual para el centro con código "35009139".
* ?opcion=1 & codigoCentro=35009139

### B) Solicitud de entradas públicas del centro con idCentro = "561EBA45-51E5-4E3F-BA6B-C4CBB8363079" desde el día 01/06/2022.
* ?opcion=2 & idCentro=561EBA45-51E5-4E3F-BA6B-C4CBB8363079 & fechaDesde=2022-06-01

### C) Solicitud de entradas públicas del centro con código "35010488" desde el 01/01/2020 hasta el 05/09/2024.
* ?opcion=1 & codigoCentro=35010488 & fechaDesde=2020-01-01 & fechaHasta=2024-09-05
