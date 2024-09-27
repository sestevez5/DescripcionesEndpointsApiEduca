# Descripción general.

Este endpoint proporciona información detallada de todos los apuntes de seguimiento (fecha, hora, motivo, tipo, etc.) asociados a una matrícula a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.  

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. ef1e4d24-f728-4c69-9b95-91668ba2c4fd)
* **soloFaltas**:
  * Si se no se establece valor o se elige "No", se devolverán los apuntes de seguimiento de cualquier tipo (Ej. Anotación positiva, Salida anticipada justificada, etc.).
  * Si se escoge el valor "Sí", solo devolverá los apuntes con el atributo "EsFalta = 1" (Ej. Falta justificada, Retraso sin justificar, etc.).
* **fechaHoraDesde**: Si se indica, solamente se devolverán los apuntes cuya fecha y horaFin sea igual o posterior a la especificada (Ej. 2024-03-06T13:00:00)
* **fechaHoraHasta**: Si se indica, solamente se devolverán los apuntes cuya fecha y horaInicio sea igual o anterior a la especificada (Ej. 2024-05-06T10:45:00)
* **codigoArea**: Si se establece, devolverá únicamente los apuntes asociados a la matrícula correspondientes al área con el código especificado (Ej. FCT).
* **soloUltimosApuntes**: Si se indica un valor (entero positivo), devolverá únicamente los últimos apuntes especificados por dicho número (Ej. 10 devolverá los últimos diez apuntes de seguimiento).
* **tipoApunte**: Si se establece (cadena de texto), se devolverán únicamente los apuntes cuyo código se haya especificado en este campo (Ej. FI proporciona solo las faltas sin justificar).

**Observaciones**:
Los valores de los códigos del parámetro **tipoApunte** son los correspondientes al campo *Codigo* de la tabla XFA_TTiposApuntesSeguimiento (ND, FJ, FI, AP, etc.).

# Ejemplos.
### A) Solicitud de solo las faltas para la matrícula con idMatricula = "ef1e4d24-f728-4c69-9b95-91668ba2c4fd" el día 12/03/24 entre las 08:00:00 y las 14:00:00.
* ef1e4d24-f728-4c69-9b95-91668ba2c4fd/apuntes-seguimiento-matricula?soloFaltas=true & fechaHoraDesde=2024-03-12T08:00:00 & fechaHoraHasta=2024-03-12T14:00:00

### B) Solicitud de todos los apuntes de seguimiento del área con código = "MAT" para la matrícula con idMatricula = "ef1e4d24-f728-4c69-9b95-91668ba2c4fd".
* ef1e4d24-f728-4c69-9b95-91668ba2c4fd/apuntes-seguimiento-matricula?codigoArea=MAT

### C) Solicitud de los 5 últimos apuntes de seguimiento con tipoApunte = "AP" (Codigo = "Anotación positiva") para la matrícula con idMatricula = "ef1e4d24-f728-4c69-9b95-91668ba2c4fd".
* ef1e4d24-f728-4c69-9b95-91668ba2c4fd/apuntes-seguimiento-matricula?soloFaltas=false & soloUltimosApuntes=5 & tipoApunte=AP

### D) Solicitud de las últimas 8 faltas injustificadas (tipoApunte = FI) del área con código = "EFI" hasta el día 30/05/2024 a las 14:00:00 para la matrícula con idMatricula = "ef1e4d24-f728-4c69-9b95-91668ba2c4fd".
* ef1e4d24-f728-4c69-9b95-91668ba2c4fd/apuntes-seguimiento-matricula?soloFaltas=true & fechaHoraHasta=2024-05-30T14:00:00 & codigoArea=EFI & soloUltimosApuntes=8 & tipoApunte=FI
