# Descripción general

Este endpoint devuelve la colección de alumnado con NEAE. Nótese que una NEAE se establece sobre una matrícula y no sobre un/a alumno/a. 

Las NEAE tienen un periodo de vigencia que, por defecto, coincide con el curso escolar completo, pero el rango de vigencia puede ser más reducido. 
Por otro lado, es importante señalar que pueden establecerse múltiples NEAE sobre una misma matrícula, siempre y cuando estas no se solapen en el tiempo. Esto ocurre cuando, por ejemplo, hay una revisión de una NEAE y se considera oportuno alterar las condiciones. No debe modificarse la NEAE original, puesto que podría afectar al registro en materia de evaluación del alumno hasta la fecha, pudiendo tener consecuencias indeseables en materia de evaluación.

## Parámetros comunes
* **opcion**: 1, 2. Se deberá escoger una obligatoriamente.
* **nivelDetalle**: r, m, e (reducido, medio, extendido). Si no se indica, su valor por defecto será r.
* **fechaReferencia**: Es un parámetro no obligatorio y, en caso de que se omita, se considerará la fecha del sistema. Solo se devolverán las neae vigentes a la fecha indicada (o del sistema si no se especifica)

## Parámetros específicos

### Opción 1
* **codigoCentro**: Campo Obligatorio (Ej.: 38010773)
* **cursoEscolar**: Campo Obligatorio (Ej.: 2024)
* **idEstudioSC**: Campo no obligatorio. Debe tomar un valor que se corresponda con el identificador de algún estudio definido en el Plan de Estudios de Canarias.
* **codigoGrupoClase**: Campo no obligatorio. Debe tomar un valor que se corresponda con el código de un grupo establecido en la aplicación Pincel Ekade.


### Opción 2
* **idCursoCentro**: Campo obligatorio. Debe corresponderse con un valor GUID de la entidad "CursoCentro" en Pincel Ekade.
* **idGrupo**: Campo no obligatorio. Debe corresponderse con un valor GUID de la entidad "Grupo". Solo se tendrán en cuentas los grupos clase.
* **idEstudio**: Campo no obligatorio. Debe corresponderse con un valor GUID de la entidad "Estudio" en Pincel Ekade. 

**Observaciones**: Esta opción está orientada a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros. 


# Ejemplos.
### A) Obtener todas las NEAE registradas en el centro con código 35010488 en el curso escolar 2024 activas en la fecha de la ejecución.
* /gestionacadcentros/neaes?opcion=1 & cursoEscolar=2024 & codigoCentro=35010488

### B) Obtener todas las NEAE registradas en el centro con código 35010488 en el curso escolar 2024 que estén activas el 25/12/2024.
* /gestionacadcentros/neaes?opcion=1 & cursoEscolar=2024 & codigoCentro=35010488 & fechaReferencia=2024-03-30

### C) Obtener todas las NEAE registradas en el cursoCentro con identificador interno "561EBA4551E54E3FBA6BC4CBB8363079".
* /gestionacadcentros/neaes?opcion=2 & idCursoCentro=561EBA4551E54E3FBA6BC4CBB8363079
