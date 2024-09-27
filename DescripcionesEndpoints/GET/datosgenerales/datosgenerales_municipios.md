# Descripción general.

Este endpoint devuelve los nombres de todos los municipios establecidos en el catálogo general de la administración educativa del Gobierno de Canarias (Ej. Agaete, Santoña, Vélez-Blanco).

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), existen otros, también opcionales, que modulan la respuesta.

## Parámetros específicos.

* **codigoIsla**: Si se indica, devuelve los municipios según los siguientes códigos: 1 (*Fuerteventura*), 2 (*Lanzarote*), 3 (*Gran Canaria*), 4 (*La Gomera*), 5 (*El Hierro*), 6 (*La Palma*), 7 (*Tenerife*).
  * Si no se indica y el parámetro **soloMunicipiosCanarias** tiene los valores *No establecido* o *Sí*, devuelve todos los municipios de la Comunidad Autónoma de Canarias. 
* **codigoProvincia**: Si se indica, devuelve los municipios de la correspondiente provincia (Ej. 35 *Las Palmas de Gran Canaria*, 39 *Cantabria*).
* **fechaReferencia**:
* **denominacionContiene**:
* **soloMunicipiosCanarias**:

**Observaciones**: Todos los parámetros específicos son opcionales, de modo que si no se indica ninguno, se devuelven todos los municipios canarios.

# Ejemplos.

### A) Solicitud de los municipios de la isla de La Palma.
* ?codigoIsla=6

