# Descripción general.

Este endpoint proporciona el conjunto de documentos asociados a una necesidade específica de atención educativa (NEAE) vinculada a una matrícula de un alumno/a de un centro educativo a partir del identificador interno de la misma.

La estructura devuelta ofrece, entre otras propiedades, la propiedad "contenido" que será array de byte codificado en Base64.

## Parámetros específicos.

* **idNeae**: Obligatorio (Ej. 4344A82F5C054067A7FF221C071A4FBB).

# Ejemplos.
## A) Solicitud de los documentos asociados a una NEAE cuyo identificador interno es "4344A82F5C054067A7FF221C071A4FBB".

* /gestionacadcentros/neaes/4344A82F5C054067A7FF221C071A4FBB/documentos-neae

