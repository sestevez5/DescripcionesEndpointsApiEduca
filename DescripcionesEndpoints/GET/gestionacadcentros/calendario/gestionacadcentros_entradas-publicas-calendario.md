# Descripción general.

Este endpoint devuelve la colección de entradas públicas del calendario, es decir, aquellas que son visibles para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*).

## Parámetros comunes.

* **opcion**: 1, 2. Se deberá escoger uno obligatoriamente.
* **fechaDesde**: Si se indica, devuelve las entradas con fecha y hora igual o posterior a la especificada (Ej. 2023-05-01T09:30:00).
* **fechaHasta**: Si se indica, devuelve las entradas con fecha y hora igual o anterior a la especificada (Ej. 2023-03-15T14:00:00).

**Observaciones**:
* En el caso de no establecerse los parámetros *fechaDesde* y *fechaHasta*, se utilizarán los del periodo administrativo del curso escolar actual a fecha del sistema.
* Opción 1: Devuelve las entradas públicas a partir del *codigoCentro* (obligatorio).
* Opción 2: Devuelve las entradas públicas a partir del *idCentro* (obligatorio).

## Parámetros específicos.

### Opción 1.
* **codigoCentro**: Obligatorio (Ej. 38010773)

**Observaciones**: El parámetro *idCentro* no está permitido en esta opción.

### Opción 2.
* **idCentro**: Obligatorio (Ej. 7C6F144112B74D5996AA55AD4BE7662F).

**Observaciones**: El parámetro *codigoCentro* no está permitido en esta opción.

# Ejemplos.
### A) Solicitud de entradas públicas del curso escolar actual para el centro con código "35009139".
* /gestionacadcentros/entradas-publicas-calendario?opcion=1 & codigoCentro=35009139

### B) Solicitud de entradas públicas del centro con idCentro = "561EBA4551E54E3FBA6BC4CBB8363079" desde el día 01/06/2022.
* gestionacadcentros/entradas-publicas-calendario?opcion=2 & idCentro=561EBA4551E54E3FBA6BC4CBB8363079 & fechaDesde=2022-06-01

### C) Solicitud de entradas públicas del centro con código "35010488" desde el 01/01/2020 hasta el 05/09/2024.
* gestionacadcentros/entradas-publicas-calendario?opcion=1 & codigoCentro=35010488 & fechaDesde=2020-01-01 & fechaHasta=2024-09-05

