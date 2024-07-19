# Descripción general

Existen endpoints para la obtención de actividades de entidades susceptibles de disponer de horario: matrículas (alumnado), docentes-servicio (docentes), pas-servicio (personal de administración y servicios), grupos y dependencias cuando se dispone de su identificador único interno. Sus _paths_ son los siguientes.

* ../gestionacadcentros/matriculas/{idMatricula}/actividades-horario.
* ../gestionacadcentros/docentes-servicio/{idDocenteServicio}/actividades-horario. 
* ../gestionacadcentros/pas-servicio/{idPasServicio}/actividades-horario. 
* ../gestionacadcentros/grupos/{idGrupo}/actividades-horario.
* ../gestionacadcentros/dependencias/{idDependencia}/actividades-horario.

Este endpoint tiene la misma funcionalidad que los anteriores, solo que no se exige el identificador único interno como parámetro. En su defecto, ofrecerá conjuntos de parámetros que identificarán de forma única a las distintas entidades.

# Parámetros
Dispondremos de 5 paquetes de parametrización, cada uno especializado en la localización de un tipo de entidad. Todos las opciones tendrán un conjunto mínimo común de parámetros.

## Parámetros comunes
### Parámetros:
Los parámetros comunes a todas las opciones son:
* **opcion.**
* **cursoEscolar.**
* **codigoCentro.**
* **fechaReferenciaHorario.**
* **horarioCompleto.**

### Observaciones:
* El parámetro "opcion" es obligatorio y podrá tomar los valores: 1, 2, 3, 4 y 5. Cada valor se corresponde con un tipo de entidad.
> * Opción 1: horario de alumnado, más correctamente, de matrículas.
> * Opción 2: horario de docentes, más correctamente, de servicios del personal docente.
> * Opción 3: horario de no docentes, más correctamente, de servicios del personal de administración (PAS).
> * Opción 4: horario de grupos.
> * Opción 5: horario del aulas, más correctamente, de dependencias.
* Los parámetros "cursoEscolar" y "codigoCentro" son obligatorios e, independientemente de la opción elegida, contextualizarán la solicitud de un horario en un centro y curso escolar.
* El parámetro "fechaReferenciaHorario" no es obligatorio y, en caso de cumplimentarse, se filtrarán aquellas actividades con vigencia en la fecha pasada como parámetro. En caso contrario (que no se cumplimente), se tendrá en cuenta la fecha del sistema si esta se encuentra en el intervalo del curso escolar pasado como parámetro. En caso contrario se considerará como fecha de referencia la última fecha del periodo administrativo del curso escolar pasado como parámetro. **Importante: este parámetro no será tenido en cuenta si el parámetro "horarioCompleto" tiene el valor "No"**
* El parámetro "horarioCompleto" no es obligatorio y su valor por defecto será "No". Si su valor es "Sí" no se realiza ningún filtro en base a la vigencia de las actividades y, por tanto, no se tendrá en cuenta el valor que pudiese tener el parámetro "fechaReferenciaHorario".


## Parámetros específicos de la opción 1
Con los parámetros ofrecidos en esta opción, en combinación con los parámetros comunes de carácter obligatorio: "cursoEscolar" y "codigoCentro", podemos identificar de forma única una matrícula.

### Parámetros:
* **nifnieAlumnado** 
* **cialAlumnado**
* **fechaReferenciaMatricula** 
* **idEstudioSC** 

### Observaciones:
* Hay que establecer alguno de los parámetro identificativos del alumnado en esta opción: nif, nie o cial.
* El parámetro "fechaReferenciaMatricula" no es obligatorio. Si se omite se considerará la fecha del Sistema
* El parámetro "idEstudioSC" es obligatorio e identifica el estudio de la matrícula según lo establecido en el Plan de Estudios de Canarias.

## Parámetros específicos de la opción 2
Con los parámetros ofrecidos en esta opción, en combinación con los parámetros comunes de carácter obligatorio: "cursoEscolar" y "codigoCentro", podemos identificar de forma única un servicio de un nombramiento.
### Parámetros:
* **nifNieDocente**: 
* **fechaReferenciaServicioDocente**: 
### Observaciones:
* El parámetro "nifNieDocente" es obligatorio.
* El parámetro "fechaReferenciaServicioDocente" no es obligatorio. Si se omite se considerará la fecha del Sistema

## Parámetros específicos de la opción 3
Con los parámetros ofrecidos en esta opción, en combinación con los parámetros comunes de carácter obligatorio: "cursoEscolar" y "codigoCentro", podemos identificar de forma única un servicio de un personal de administracion y servicios.
### Parámetros:
* **nifNiePas**: 
* **fechaReferenciaServicioPas**: 
### Observaciones:
* El parámetro "nifNiePas" es obligatorio.
* El parámetro "fechaReferenciaServicioPas" no es obligatorio. Si se omite se considerará la fecha del Sistema

## Parámetros específicos de la opción 4
Con los parámetros ofrecidos en esta opción, en combinación con los parámetros comunes de carácter obligatorio: "cursoEscolar" y "codigoCentro", podemos identificar de forma única un grupo.
### Parámetros:
* **codigoGrupo**
### Observaciones:
* El parámetro "codigoGrupo" es obligatorio. 

## Parámetros específicos de la opción 5
Con los parámetros ofrecidos en esta opción, en combinación con los parámetros comunes de carácter obligatorio: "cursoEscolar" y "codigoCentro", podemos identificar de forma única una dependencia. 
### Parámetros:
* **codigoDependencia**
### Observaciones:
* El parámetro "codigoDependencia" es obligatorio.  

## Notas: 

* Elegida una de las opciones a través del campo "opcion" no deberá pasarse ningún parámetro específico distinto a la opción elegida. 

# Ejemplos.
## A) Solicitud del horario de un docente
Obtener el horario de un docente con un identificador de servicio _e4297da2-b2bb-4505-819f-66f3b8e051f3_
> * ?opcion=1 & idDocenteServicio=e4297da2-b2bb-4505-819f-66f3b8e051f3
## B) Solicitud del horario de una alumna (Variante 1)
Obtener el horario de la alumna con cial _B05A26124Q_ correspondiente a su matrícula "vigente" en el centro _38010111_ en el curso escolar 2022. Solo las actividades registradas en el horario que estén "vigentes".
> * ?opcion=2 & cursoEscolar=2022 & codigoCentro=38010111 & cialAlumnado = B05A26124Q
## C) Solicitud del horario de una alumna (Variante 2)
Obtener el horario de la alumna con cial _B05A26124Q_ correspondiente a su matrícula vigente el 2/9/2022 en el centro _38010111_ en el curso escolar 2022. Se solicitan TODAS las actividades.
> * ?opcion=2 & cursoEscolar=2022 & codigoCentro=38010111 & cialAlumnado = B05A26124Q & fechaReferenciaMatricula="2022-09-02" & horarioCompleto=Si
## D) Solicitud de la ocupación de un aula. 
Obtener el horario del aula "A1.2" del centro eductivo _35666111_ en el curso escolar 2020.
> * ?opcion=5 & cursoEscolar=2022 & codigoCentro=35666111 & codigoDependencia = A1.2.



