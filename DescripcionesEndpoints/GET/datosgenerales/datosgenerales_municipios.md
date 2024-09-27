# Descripción general.

Este endpoint devuelve los nombres de todos los municipios de las Islas Canarias (Ej. Agaete, Tegueste).

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), existen otros, también opcionales, que modulan la respuesta.

## Parámetros específicos.

* **codigoIsla**: Si se indica, devuelve los municipios correspondientes al código: 1 (*Fuerteventura*), 2 (*Lanzarote*), 3 (*Gran Canaria*), 4 (*La Gomera*), 5 (*El Hierro*), 6 (*La Palma*), 7 (*Tenerife*).
* **codigoProvincia**: Si se indica, devuelve los municipios de la provincia correspondiente: 35 (*Las Palmas de Gran Canaria*), 38 (*Santa Cruz de Tenerife*).
* **fechaReferencia**:
* **denominacionContiene**:
* **soloMunicipiosCanarias**:

**Observaciones**: Todos los parámetros específicos son opcionales, de modo que si no se indica ninguno, se devuelven todos los municipios canarios.

# Ejemplos.

### A) Solicitud de los municipios de la isla de La Palma.
* ?codigoIsla=6

