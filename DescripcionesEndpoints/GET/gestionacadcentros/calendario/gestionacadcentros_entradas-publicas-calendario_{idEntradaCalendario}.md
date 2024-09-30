# Descripción general.

Este endpoint devuelve una entrada pública del calendario, es decir, que es visible para toda la comunidad educativa (idNivelPrivacidad = 2 en *dbo.XCA_EntradasCalendario*) a partir del parámetro *idEntradaCalendario*, por lo que está orientado a aplicaciones consumidoras que conocen identificadores internos de Pincel de las entidades que representan los parámetros.

## Parámetros específicos.

* **idEntradaCalendario**: Obligatorio (Ej. 0487229980B0400D8DF4A0CF0F1B6BB1)

# Ejemplos.
### A) Solicitud de la entrada pública con idEntradaCalendario = "04872299-80B0-400D-8DF4-A0CF0F1B6BB1".
* /gestionacadcentros/entradas-publicas-calendario/0487229980B0400D8DF4A0CF0F1B6BB1
