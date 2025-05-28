# Descripción general.

Este endpoint devuelve una colección de centros educativos registrados en el Directorio de Centros de la Consejería de Educación del Gobierno de Canarias. 
## Parámetros específicos.

* **nivelDetalle**: Se dispone de dos niveles de detalle: r y m, siendo r el valor por defecto.
* **codEtapaCentro**: Se podrá filtrar por tipología de centros a partir de un código de una de las tipologías. La lista de tipos de centros (etapasCentro) se podrá obtener a partir del endpoint "directorio-centros/etapas-centro"
* **isla**: Se podrá filtrar por isla a través de su código. Se podrán obtener a partir del endpoint "datos-genereales/islas".
* **codigoMunicipio**: Se podrá filtrar por municipio a través de su código. Se podrán obtener a partir del endpoint "datos-genereales/municipios".
* **naturaleza**: La naturaleza de un centro responde a características como "privado", "público". Podemos obtener la lista de esta categoría a partir del endpint "directorio-centros/naturalezas-centro"
* **zonaInspeccion**: Los centros educativos están circunscritos a zonas de inspección. Las zonas de inspección se pueden obtener a partir del endpoint "directorio-centros/zonas-inspeccion".  Se podrá filtrar por zonas de inspección a través de su código.


# Ejemplos.
### A) Solicitud de la lista de centros educativos de carácter privado de la isla de Lanzarote.
* /gestionacadcentros/centros?isla=1 & naturaleza=2  

### B) Solicitud de la lista de centros educativos del municipio de Santa Úrsula.
* /gestionacadcentros/centros ? municipio=38390