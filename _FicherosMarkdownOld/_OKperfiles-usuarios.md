# Descripción general

En la Gestión Académica y Administrativa de Centros Educativos existen 4 posibles perfiles: responsables, alumnado, docentes y personal de administración y servicios (PAS). Estos perfiles quedan catálogados con los literales siguientes:

* "RES" --> Responsables
* "DOC" --> Docentes
* "ALU" --> Alumnado
* "PAS" --> Personal de administración y servicios.

# Nivel de detalle de la devolución. 
Este endpoint ofertará la posibilidad de indicar el nivel de detalle de información en cuanto a la información devuelta:

## Nivel de detalle "reducido". 

En este nivel de detalle, básicamente, se devuelve un array de objetos muy simples. Cada objeto representa a uno de los colectivos al que pertenece el usuario. 

## Ejemplo

~~~
[
    {
    "tipoPerfil": "RES"
    },
    {
    "tipoPerfil": "DOC"
    }
}
~~~

El devolución del ejemplo nos indica que el usuario es responsable y docentes dentro del Sistema. No se da más información acerca de los datos que le otorgan estos perfiles.



## Nivel de detalle "medio". 

Con este nivel de detalle se amplía la información devuelta, incorporando información del identificador del usuario en el colectivo y el identificador del centro educativo que le otorga el perfil.


## Ejemplo

~~~
[
    {
    "tipoPerfil": "RES",
    "idEntidad": "5f05313d-f0df-44a3-bf03-d853d6d99f0b",
    "idCentro": "e70b02b6-d356-4a18-a7f2-1b7df48723a1",
    },
      {
    "tipoPerfil": "DOC",
    "idEntidad": "c865ab57-dab5-4ac1-ab9f-6af1210e3c30",
    "idCentro": "c53ee2d0-9db9-411f-b341-9526edf85eb8",
    },
     {
    "tipoPerfil": "RES",
    "idEntidad": "bc5d5c2e-912d-4080-a1fb-cb4a70d1d2a7",
    "idCentro": "4520bba5-3e46-4054-aede-f3b74310c04c",
    }
}
~~~

La devolución del ejemplo anterior se corresponde con un usuario que:

1. Es responsable de, al menos, un alumno en el centro con identificador "e70b02b6-d356-4a18-a7f2-1b7df48723a1" y su identificador como responsable en dicho centro es "5f05313d-f0df-44a3-bf03-d853d6d99f0b".

2. Es docente en el centro con identificador "c53ee2d0-9db9-411f-b341-9526edf85eb8" y su identificador como docente en dicho centro es "c865ab57-dab5-4ac1-ab9f-6af1210e3c30".

3. Es responsable de, al menos, un alumno en el centro con identificador "4520bba5-3e46-4054-aede-f3b74310c04c" y su identificador como responsable en dicho centro es "bc5d5c2e-912d-4080-a1fb-cb4a70d1d2a7".



## Nivel de detalle "extendido". 

Con este nivel de detalle se amplía la información devuelta, incorporando información personal.


## Ejemplo

~~~
[
    {
    "tipoPerfil": "RES",
    "idEntidad": "5f05313d-f0df-44a3-bf03-d853d6d99f0b",
    "idCentro": "e70b02b6-d356-4a18-a7f2-1b7df48723a1",
	"nombre": "Jacinto",
    "primerApellido": "Galoro",
    "segundoApellido": "Mora",
    "nombreSentido": null,
    "idUltimaFoto": null,
    "sexo": "Varón",
    "sexoSentido": null
    },
      {
    "tipoPerfil": "DOC",
    "idEntidad": "c865ab57-dab5-4ac1-ab9f-6af1210e3c30",
    "idCentro": "c53ee2d0-9db9-411f-b341-9526edf85eb8",
	"nombre": "Jacinto",
    "primerApellido": "Galoro",
    "segundoApellido": "Mora",
    "nombreSentido": null,
    "idUltimaFoto": "483cce5f-37f0-41ba-bfe3-235fe2c7759c",
    "sexo": "Varón",
    "sexoSentido": null
    },
     {
    "tipoPerfil": "RES",
    "idEntidad": "bc5d5c2e-912d-4080-a1fb-cb4a70d1d2a7",
    "idCentro": "4520bba5-3e46-4054-aede-f3b74310c04c",
	"nombre": "Jacinto",
    "primerApellido": "Galoro",
    "segundoApellido": "Mora",
    "nombreSentido": null,
    "idUltimaFoto": null,
    "sexo": "Varón",
    "sexoSentido": null
    }
}
~~~