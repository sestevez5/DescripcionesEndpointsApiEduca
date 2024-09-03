# Descripción.
ApiEduca es un API REST que expone las entidades que se gestionan en la Herramienta de Gestión Académica y Administrativa de los centros educativos (Pincel Ekade). No obstante, de forma temporal, también se han incluidos entidades externas como, por ejemplo, algunas de las gestionadas en el Directorio de Centros o el Plan de Estudios de Canarias.

# Seguridad.
ApiEduca es un Api de carácter interno y su consumo solo puede realizarse a través de la Intranet Corporativa . Además, es condición necesaria disponer de un ApiKey para su acceso. Este ApiKey tendrá asociado unos niveles de autorización que, en buena parte, marcarán los privilegios de acceso y manipulación de los recursos expuestos.

Existen determinados endpoints en los que disponer de un ApiKey con los privilegios necesarios no nos aporta el acceso a los mismos. Dichos endpoints requieren de una autenticación personal. ApiEduca provee de diferentes endpoints para realizar la autenticación cubriendo las diferentes casuísticas. Ver [Anexo I](#AnexoI)

# Generalidades.
Se ha intentado imprimir la máxima regularidad en la implementación de los endpoints que conforman este Api con el objetivo de normalizar su desarrollo y, a la par, simplificar su consumo.  En este apartado describiremos lo que, a nuestro juicio, en conveniente conocer por su carácter transversal, evitando, así, reiterar las mismas especificaciónes en diferentes Endpoints.

# Estructura de los endpoints.

Podemos distinguir tres unidades de información en los endpoints: servidor, sistema y segmentos propios del endpoint.

* Disponemos de dos entornos: preproducción y producción. El segmento unicial de las uris correspondientes a los endpoints en cada entorno serán: https://wwwpre.educacion.org/educacion/bussed/apieduca y https://www.gobiernodecanarias.org/educacion/bussed/apieduca.
* Los endpoints estarán dentro de un sistema y dicho sistema se identificará en el primer segmento. Justo el segmento que sigur al indicado en el punto anterior.

Veamos algunos ejemplos:

Ejemplo 1: https://www.gobiernodecanarias.org/educacion/bussed/apieduca/centros/zonas-inspeccion: endpoint que devuelve las diferentes zonas de inspección que se han establecidos en materia de educación en la Comunidad Canarias. Es una gestión correspondiente al Directorio de Centros y, por tanto, el "sistema" es "centros". En este caso, atendiendo al comienzo de la uri podemos ver que se trata de un endpoint del entornod e producción.
Ejemplo 2: https://wwwpre.educacion.org/educacion/bussed/apieduca/gestionacadcentros/matriculas: endpoint de que devuelve una colección de matrículas del entorno de preproducción. Se trata de información proveniente de Pincel Ekade. La sección del endpoint que sistema que representa a todas las entidades provenientes de Pincel Ekade es  "gestionacadcentros" (Gestión académica y administrativa de centros).


## Estructura de las respuestas.
Las respuestas a las peticiones a cualquier petición de ApiEduca siempre tiene la misma estructrura JSON. Se trata de un objeto que actúa como envoltura (wrap) ante cualquier petición. Este objeto unificado de respuesta tiene 3 campos: datos, mensajes y metadatos.

### Datos.
Este campo devuelve los datos solicitados (generalmente, ante peticiones GET). Distinguiremos entre colecciones (devolución de un array) y entregas simples (devolución de un objeto). En el desarrollo de ApiEduca hemos creado un catálogo de DTO's (Data Tranfer Object) que representa la interfaz al exterior de las entidades que gestionamos y cuyo objetivo es dar legibilidad, desacoplar las respuestas a las estructuras internas y ocultar aspectos irrelevantes a los consumidores.
En el apartado "colecciones" veremos cómo, en ocasiones, disponemos de representaciones polimórficas de estas entidades a través de la definición de múltiples DTO's, permitiéndonos equilibrar la necesidad de información con el rendimiento de las respuestas y también con niveles de seguridad en base al contenido expuesto.

### Mensajes.
Este campo devuelve una colección de mensajes (potencialmente vacío). En muchas ocasiones es necesario acompañar las respuestas con mensajes que aporten información adicional a los consumidores, los cuales pueden ir desde meros avisos hasta notificaciones de errores. Por ejemplo, el sistema, ante una petición incorrectamente formada, notificará de este hecho al peticionario. También es el mecanismo habitual cuando se realiza una petición que incumple reglas de negocio establecidas (Ej. "La fecha de finalización de una matrícula no puede ser anterior a la fecha de matrícula").

### Metadatos.
Este campo es, precisamente, el que nos ha llevado a optar por el uso de envolvente a las respuestas. Se trata de un objeto que nos permite aportar información sobre la propia gestión de la petición. A nivel básico, aporta, entre otros datos, la fecha/hora de la petición, usuario autenticado, url de la solicitud, etc. En determinadas ocaciones estos medadatos se enriquecen con informacióin adicional. Tal es el caso de las respuestas de peticiones que devuelven colecciones. En estos casos se aporta información adicional como, por ejemplo, datos de paginación, filtro y orden.

## Códigos de respuesta.
En función de la naturaleza de las peticiones o del resultado obtenido al procesar una petición nos podemos encontrar con múltiples casuísticas. Hemos intentado ajustarnos a la semántica establecida en el protocolo HTTP en lo relativo a los códigos de respuestas. Con carácter general se devuelve un subconjunto de códigos que intentamos describir a continuación.

- **200** (_OK_): las respuestas acompañadas con esté código responden a dos casos bien diferenciados, aunque ambos tienen en común que reflejan peticiones que han podido ser procesadas de forma satisfactoria:
    - Se devuelve al usuario el contenido solicitado.
    - Lo solicitado por el usuario ha sido satisfactoriamente procesado pero la lógica de la aplicación establece que no debe aportarse la información requerida.
Es importante destacar que la intención primera de codificación del segundo caso era un código de respuesta 204 (No content). Sin embargo esto no es posible puesto que el protocolo no permite que se envíe contenido en el "body" de la respuesta y, en el caso de usar envolventes, siempre vamos a requerir devolver contenido.
- **201** (_Created_): es el código de respuesta ante una petición en la que se solicita la creación de un recurso y ha sido satisfactoria.
- **203** (_Non-Authoritative Information_): es el código de respuesta que damos ante una petición habilitada para un cliente que ha podido ser atendida pero la lógica de la aplicación establece que no debe aportarse la información requerida. Un ejemplo de respuesta con este código podría ser la solicitud de sesiones de evaluación no publicadas para ciertas aplicaciones.
- **400** (_Bad Request_): es el código de respuesta ante una petición que no puede ser atendida por estar mal formada, por no seguir las directrices de la especificación de los parámetros query, etc. En resumen, estamos ante peticiones que no pueden ser resueltas de forma satisfactoria.
- **401** (_Unauthorized_): como indica su descripción se da esta respuesta cuando el cliente no está autorizado a consumir el endpoint. Puede deberse a que el usuario no ha hecho uso de un token o que la información del token establece que el cliente no es apto para el consumo del endpoint.
- **403** (_Forbidden_): este código de respuesta solo se devuelve cuando se hace uso de endpoints dirigidos a la autenticación y, fruto del procesado de la petición se dictamina que la autenticación es insatisfactoria. Por ejemplo, no se obtiene un token debido a credenciales no válidas.
- **409** (_Conflict_): se devuelve cuando se ejecuta un endpoint de manipulación de un recurso (métodos POST, PUT, DELETE, PATCH ) y hay una o varias reglas de negocio que impiden la ejecución de la acción solicitada. Se devolverá en el nodo "mensajes" la colección de reglas que se incumplen.
- **500** (_Internal Server Error_): no se establece ningún desglose. Aparece este error ante excepciones internas de la aplicación.

## Colecciones.

### Parámetros de carácter general.
Los endpoints de tipo GET que devuelven colecciones de datos conforman el conjunto más representativo de endpoints de ApiEduca y, probablemente, el más demandado. Es muy importante, por tanto, aportarle la suficiente flexibilidad para que cubra las necesidades de la mayoría de los consumidores, aunque evitando dar respuestas sobreajustadas que provoquen un exceso de configuraciones que compliquen su uso e implementación. Como respuesta a la flexibilidad hemos uniformado los parámetros que establecen especificaciones de carácter general, tanto en lo referente a la información devuelta como en la oferta de parámetros. Son los siguientes:

- **Nivel de detalle**: muchos de los endpoints que devuelven colecciones de objetos nos permite establecer el nivel de información devuelta en estos objetos. Es decir, nos permiten establecer la estructura de los objetos devueltos. El parámetro es "nivelDetalle" y sus valores posibles son "r"(reducido), "m"(medio) y "e"(extendido), aunque puede que algunos endpoints no ofrezcan todos los niveles. Es obvio que el uso del nivel reducido redundará en una mejora del rendimiento. En general, se aconseja usar siempre el nivel mínimo que aporte la información requerida.
En este punto hay otro aspecto a destacar y es el relacionado con la seguridad. Puede que a determinados usuarios solo se les permita hacer uso de niveles reducidos de contenido debido a que los extendidos exponen información a la que dichos usuarios no están autorizados a acceder.

- **Opcion**: en algunos de los endpoints que devuelven colecciones se permite aplicar filtros de diferentes formas. Cada una de esas formas es lo que denominamos "opción". En la descripción de cada endpoint de especifica los parámetros que conforman cada una de las opciones.

- **Paginación**: posicionInicial y tamanyoBloque: como es obvio, debemos establecer un sistema de paginación ante endpoints que devuelven colecciones de entidades. Hemos definido dos parámetros para establecer la página requerida en la respuesta a través de la posición inicial del paquete solicitado y el número de datos requerido. Por ejemplo, si indicamos en el parámetro "posicionInicial" el valor 4 y al parámetro "tamanyoBloque" el valor 70, el sistema devolverá la cuarta página de un sistema de bloques de 70 registros.
En caso de omisión de estos parámetros se devolverá la primera página de una paginación de bloques de tamaño 100. (posicionIniciao=0 y tamanyoBloque=100).

### Orden <pendiente>

## [Anexo I]{#AnexoI} 

La autenticación en ApiEduca, como la mayoría de Apis de tipo ApiREST, está basada en tokens. En concreto, en el modelo JWT Bearer. Por tanto, como paso previo a cualquier invocación de endpoints necesitamos obtener un token váldio.

Para la obtención del token disponemos de varias opciones (endpoints). Estos endpoint son los siguientes:

* /seguridad/autenticacion-por-aplicacion
* /seguridad/autenticacion-por-guidsesion
* /seguridad/autenticacion-por-usuario

Los tres endpoints tienen en común que requieren como parámetro la ApiKey que representa a la aplicación consumidora.  El primero de ellos (por aplicación) no requiere ningún otro parámetro y, por tanto, no se le traslada información relativa a ningún usuario. Obviamente, haciendo uso de este endpoint para generar el token de autenticación vamos a tener restricciones en el consumo de determinados endpoints: aquellos que requieren de un usuario para su consumo.


Los otros dos endpoint ( por guidsesion y usuario ) requerirán información de un usuario. 

El primero hará uso de un guissesion proveniente del sistema de Autenticación SUA. Es interesante cuando el consumo de los endpoints se realice a través de una aplicación que ya ha requerido la autenticación SUA y dispone, por tanto, de un guidsesion, evitando pasar por un nuevo proceso de autenticación para el consumo de ApiEduca. 

En cuanto al segundo endpoint vamos a tener que suministrarle las credenciales SUA como parámetros adicionales del endpoint y será el endpoint quien realice la autenticación a través del Sistema SUA.









