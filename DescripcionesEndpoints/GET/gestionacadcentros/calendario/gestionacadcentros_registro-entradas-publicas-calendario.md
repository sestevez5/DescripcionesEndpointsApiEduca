# Descripción general.

Este endpoint devuelve la colección de entradas públicas del calendario de un centro, es decir, aquellas que son visibles para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*).

## Parámetros específicos.

* **codigoCentro**: Obligatorio (Ej. 38010773)
* **fechaDesde**: Si se indica, devuelve las entradas con fecha igual o posterior a la especificada (Ej. 2023-05-01).
* **fechaHasta**: Si se indica, devuelve las entradas con fecha igual o anterior a la especificada (Ej. 2023-03-15).
* **tipoEntrada**: Si se indica, se devuelven solamente las entradas cuyo código coincida con el especificado, y que corresponden al parámetro _codigo_ de la tabla *XCA_TTipoEntradaCalendario* (Ej. "FES" devuelve los días festivos).

**Observaciones**:
* En el caso de no establecerse los parámetros *fechaDesde* y *fechaHasta*, se devolverán todas las entradas públicas del calendario.

# Ejemplos.
### A) Solicitud de todas las entradas públicas del centro con código "35009139" entre los días 01/09/2023 y 30/06/2024.
* /gestionacadcentros/registro-entradas-publicas-calendario?codigoCentro=35010488 & fechaDesde=2023-09-01 & fechaHasta=2024-06-30

### B) Solicitud de las entradas públicas de tipo "FES" (Día festivo) del centro con código "35009139" a partir del día 08/01/2024.
* /gestionacadcentros/registro-entradas-publicas-calendario?codigoCentro=35010488 & fechaDesde=2024-01-08 & tipoEntrada=FES
