# Descripción general
Devuelve una colección de matrículas a partir de un conjunto de paquetes de parametrización que permitirá abordar la mayoría de las necesidades requeridas por los consumidores.

# Parámetros
Dispondremos de 5 paquetes de parametrización:

## Parámetros específicos de la opción 1
Esta opción está dirigida a la obtención de una colección de matrículas correspondiente a un centro y curso escolar, pudiendo filtrar por estudio y/o grupo conociendo identificadores NO internos de estas entidades.

### Parámetros:
* **cursoEscolar**
* **codigoCentro**
* **idEstudioSC**
* **codigoGrupo**
* **fechaReferencia**

### Observaciones:
* El parámetro "cursoEscolar" es obligatorio.
* El parámetro "cursoCentro" es obligatorio.
* El parámetro "idEstudioSC" es opcional y su valor debe corresponder con el identificador de un estudio en el Plan de Estudios de Canarias.
* El parámetro "codigoGrupo" es opcional y su valor se debe corresponder con el código del grupo.
* Los parámetros "idEstudioSC" y "codigoGrupo" se pueden cumplimentar de forma conjunta, aunque, obviamente, no se obtendrán resultados en los casos en los que el grupo indicado no imparta el estudio.
* El parámetro "fechaReferencia" es opcional y, cumplimentándolo, podemos restringir la colección de matrículas a aquellas matrículas cuyo periodo de vigencia contemple la fecha indicada. 
* Puesto que los campos "idEstudioSC" y "codigoGrupo" son opcionales, cabe la posibilidad de obtener la colección de todas las matrículas de un centro en un curso escolar sin más que no establecer valorar para ellos.

## Parámetros específicos de la opción 2
Esta opción está dirigida a la obtención de una colección de matrículas correspondiente a un cursocentro, pudiendo filtrar por estudio y/o grupo a partir de sus identificadores internos.

### Parámetros:
* idCursoCentro
* idEstudio
* idGrupo, sólo válido para filtrar grupos de clase.
* fechaReferencia

### Observaciones:
* El parámetro "idCursoCentro" se debe corresponder con el identificador interno del cursoCentro en Pincel. Es obligatorio.
* El parámetro "idEstudio" es opcional y su valor se debe corresponder con el identificador de un estudio en Pincel.
* El parámetro "idGrupo" es opcional y su valor se debe corresponder con el identificador de un grupo en Pincel. Solo se tendrán en cuenta identificadores de grupos clase.
* El parámetro "fechaReferencia" tendrá el mismo comportamiento que en la opción 1.

## Parámetros específicos de la opción 3
Esta opción está dirigida a la obtención de una colección de matrículas de un/a alumno/a de un centro en un curso escolar conocido el identificador interno del alumno en el centro.

### Parámetros:
* cursoEscolar (_obligatorio_)
* idAlumnadoCentro (_obligatorio_)
* fechaReferencia

### Observaciones:
* El parámetro "cursoEscolar" es obligatorio.
* El parámetro "idAlumnadoCentro" es obligatorio. Es el identificador interno de un alumno en un centro. 
* El parámetro "fechaReferencia" tendrá el mismo comportamiento que en la opción 1.


## Parámetros específicos de la opción 4
Esta opción está dirigida a la obtención de una colección de matrículas de un/a alumno/a conocido alguno de sus identificadores (cial, nif, nie o pasaporte)

### Parámetros:
* codigoCentro
* cursoEscolar
* cial
* nifNie 
* pasaporte

### Observaciones:
* El parámetro "codigoCentro" es opcional
* El parámetro "cursoescolar" es opcional. 
* Los parámetros "cial", "nifNie" y "pasaporte" son opcionales, aunque se exige cumplimentar, al menos, uno de ellos.
* Puesto que los parámetros "codigoCentro" y "cursoEscolar" son opcionales, cabe la posibilidad de obtener todas las matrículas de un/a alumno/a en el sistema

## Parámetros específicos de la opción 5
Esta opción nos permite obtener la colección de matrículas de tutelados de un responsable identificado a partir de su nif, nie o pasaporte.

### Parámetros:

* codigoCentro
* cursoEscolar
* nifNieResponsable
* pasaporteResponsable

### Observaciones:

* El parámetro "codigoCentro" es opcional
* El parámetro "cursoescolar" es opcional
* Los parámetros "nifNieResponsable" y "pasaporteResponsable" son opcionales, aunque se exige cumplimentar, al menos, uno de ellos.

# Ejemplos.
### A) Solicitud de matrículas del centro con código "35010488" en Educación Infantil 6º ( 5 años ) (LOMLOE) (idestudio=8429) en el curso escolar 2024
* ?opcion=1 & cursoEscolar=2024 & codigoCentro=35010488 & idEstudioSC=8429

### B) Solicitud de todas las matrículas del alumno con nif "45398140G" registradas en el sistema.
* ?opcion=4 & nifNie=45398140G
