# MODIFICAR.



# Descripción general.

Este endpoint devuelve los nombres de todos los municipios establecidos en el catálogo general de la administración educativa del Gobierno de Canarias (Ej. Agaete, Santoña, Vélez-Blanco).

**Observaciones**: Aparte de los parámetros optativos de caracter general de paginación (_posicionInicial_ y _tamanyoBloque_), existen otros, también opcionales, que modulan la respuesta.

## Parámetros específicos.

* **codigoIsla**: Si se indica, devuelve los municipios según los siguientes códigos: 1 (*Fuerteventura*), 2 (*Lanzarote*), 3 (*Gran Canaria*), 4 (*La Gomera*), 5 (*El Hierro*), 6 (*La Palma*), 7 (*Tenerife*).
  * Si no se indica y el parámetro **soloMunicipiosCanarias** tiene los valores *No establecido* o *Sí*, devuelve todos los municipios de la Comunidad Autónoma de Canarias.
  * Si no se indica y el parámetro **soloMunicipiosCanarias** tiene el valor *No*, devuelve todos los municipios del catálogo general. 
* **codigoProvincia**: Si se indica, devuelve los municipios de la correspondiente provincia de la Comunidad Autónoma Canaria (Ej. 35 *Las Palmas de Gran Canaria*, 38 *Santa Cruz de Tenerife*).
  * Si no se indica y el parámetro **soloMunicipiosCanarias** tiene los valores *No establecido* o *Sí*, devuelve todos los municipios de la Comunidad Autónoma de Canarias.
  * Si no se indica y el parámetro **soloMunicipiosCanarias** tiene el valor *No*, devuelve todos los municipios del catálogo general. 
* **fechaReferencia**: Si se indica, devuelve los municipios vigentes en la fecha especificada. Si no, devuelve los municipios vigentes en la fecha del sistema.
* **denominacionContiene**: Si se pasa este parámetro, se devuelven solo los municipios cuya denominación contiene dicho parámetro.
* **soloMunicipiosCanarias**: Si se selecciona el valor *No*, incluye los municipios no pertenecientes a la Comunidad Autónoma de Canarias.

**Observaciones**: Todos los parámetros específicos son opcionales. Si no se indica ninguno, se devuelven todos los municipios canarios.

# Ejemplos.

### A) Solicitud de los municipios de la isla de La Palma.
* /datosgenerales/municipios?codigoIsla=6

### B) Solicitud de los municipios de la comunidad autónoma de Cantabria.
* /datosgenerales/municipios?codigoProvincia=39 & soloMunicipiosCanarias=false

### C) Solicitud de los municipios de la provincia de Las Palmas.
* /datosgenerales/municipios?codigoProvincia=35 & soloMunicipiosCanarias=true

