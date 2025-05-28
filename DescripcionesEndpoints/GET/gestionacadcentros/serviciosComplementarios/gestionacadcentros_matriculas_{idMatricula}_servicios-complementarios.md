
# Descripción general.

Este endpoint proporciona información de los servicios complementarios asociados a una matrícula concreta a partir del parámetro *idMatricula*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idMatricula**: Obligatorio (Ej. F0624792913E4CBBAA26225B9AC29BFC)
* **soloActivos**: Si no se establece valor, se tomará por defecto "Sí", devolviéndose en este caso solo los servicios complementarios activos. Si su valor es "No", se devolverán todos los servicios complementarios asociados a la matrícula. 

# Ejemplos.

### A) Solicitud de los servicios complementarios *activos* de la matrícula con idMatricula = "D23BF70705E84A668EDD83483496B49E".
* /gestionacadcentros/matriculas/D23BF70705E84A668EDD83483496B49E/servicios-complementarios

### B) Solicitud de *todos* los servicios complementarios, *activos* o *no*, de la matrícula con idMatricula = "D23BF70705E84A668EDD83483496B49E".
* /gestionacadcentros/matriculas/D23BF70705E84A668EDD83483496B49E/servicios-complementarios?soloActivos=false

