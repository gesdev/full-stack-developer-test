# Full-stack-developer-test
prueba técnica para evaluar las habilidades de un desarrollador de software en los siguientes aspectos: desarrollo back-end, desarrollo front-end, desarrollo de REST API y bases de datos.

Para evitar correos electrónicos rebotados, nos gustaría que envíe sus resultados bifurcando este repositorio en Github y compartiendo la URL de su repositorio con el administrador de nuestro personal. Su repositorio debe contener como minimo:

* Un único archivo de README.md con las respuestas a las preguntas técnicas
* Una carpeta "backend" que contiene la prueba técnica de backend
* Una carpeta "frontend" que contiene la prueba técnica del frontend
* Agregue el archivo README en las dos carpetas de codificación para explicar cómo ejecutar su código.
* No pida a sus amigos que resuelvan el desafío por usted. Deberá explicar sus elecciones en persona.

## Requerimientos 
* Su código debe compilarse y ejecutarse en un solo paso.
* Siéntase libre de utilizar cualquier framework/biblioteca/paquete que desee.
* Intente acercarse lo más posible a la imagen de nuestra vista de calendario.
* Su desarrollo debe funcionar con el archivo sesiones.json (al momento de ejecutar debe cargar la data del archivo a la tabla de sesiones)

### Ejemplo 
```
{
   "sesiones":{
      "Fisica I":[
         {
            "fecha_inicio":"16/04/2024 8:00",
            "fecha_fin":"16/04/2024 10:00",
            "cupo":10
         }
      ],
      "Electronica IV":[
         {
            "fecha_inicio":"16/04/2024 18:00",
            "fecha_fin":"16/04/2024 19:00",
            "cupo":20
         }
      ],
      "Matematica III":[
         {
            "fecha_inicio":"16/04/2024 11:00",
            "fecha_fin":"16/04/2024 13:00",
            "cupo":15
         }
      ]
      }
      }
```

## Que evaluaremos
* Tu código será evaluado por: semántica, estructura, legibilidad, tamaño, entre otros factores.
* Se evaluará el historial de git.
* Estamos buscando un desarrollador que sepa desenvolverse en todo el proceso de desarrollo. Utilice esta oportunidad para mostrarnos lo bueno que es en ambas áreas.
* No olvide documentar el proceso necesario para ejecutar y crear su aplicación. O si no, ¿cómo vamos a evaluar su trabajo si no podemos iniciar el proyecto en nuestras máquinas?

# Developer recruitment test
El desarrollo consiste en crear una aplicación web para participar en sesiones de clases de una universidad, para este sistema deberá seguir los requisitos solicitados en cada una de las etapas del proyecto. El sistema cuenta con una serie de sesiones donde un estudiante se puede inscribir, cada sesión cuenta con un nombre de curso, fecha inicio fecha final y cupo. Un alumno debe ser capaz de ver las sesiones disponibles para las diferentes fechas y seleccionar en cual desea participar. 

## Restricciones :
* Un alumno debe existir en el sistema previamente (en tabla alumnos) 
* Una sesión no debe permitir inscripciones después de llegar a su cupo límite
* Un alumno no puede inscribirse a 2 o más sesiones que sus horarios se entrelazan

# Backend 
1. Crear el modelo de datos, crear 3 tablas para la aplicación, estudiantes, sesiones y asignaciones.
2. Crea una tabla llamada "estudiantes" con al menos tres columnas: id (clave primaria), nombre y correo electrónico.
3. Crea una tabla llamada "sesiones" con al menos cinco columnas: id (clave primaria), nombre y start_datetime, end_datetime, cupo
4. Cree la tabla asignaciones segun consider major, esta debe tener la relacion entre un estudiante y la sesión a la que se inscribió.
5. Ingrese datos de prueba a las tablas de estudiantes y sesiones
6. Implementa endpoints para obtener información de estudiantes y sesiones.
7. Implementa endpoints para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en la tabla estudiantes.
8. Implementa endpoints para realizar operaciones CRUD (Crear, Leer, Actualizar, Eliminar) en la tabla de asignaciones.

# Front-End

Crear una aplicación Web (Si está familiarizado con un framework de front-end como React.js, Angular o Vue.js Puede utilizarlo)  que tenga el mantenimiento de latabla asignaciones (Agregar, Eliminar, Modificar), donde dicho mantenimiento debe contener:

a) Listado de fechas disponibles de sesiones (estas deben provenir de la información en la tabla de sesiones).
b) Grid de sesiones disponibles para una fecha, cada sesion debe mostrar su información básica.
c) Un grid para visualizar los datos de la tabla 3.

![Diseño aplicacion web](https://github.com/bhlr/full-stack-developer-test/blob/main/design/sesionestest.png)

La aplicación no tiene acceso a base de datos, todo se hace a través del Web API, y dejar
parametrizable la dirección del Web API.d) Página de la sesion que muestre la información básica y combobox para seleccionar alumno a asignar. 
La aplicación no tiene acceso a base de datos, todo se hace a través del Web API, y dejar
parametrizable la dirección del Web API.

# Desarrollo de REST API
### Diseño de API:
* Diseña una API RESTful para al menos tres endpoints /estudiantes, /sesiones y /asignaciones Define los métodos HTTP permitidos para cada recurso (GET, POST, PUT, DELETE) y las rutas correspondientes.
* Manejo de Solicitudes:Implementa controladores para cada método HTTP en tus recursos de API.Asegúrate de que los controladores manejen correctamente las solicitudes entrantes y realicen las operaciones correspondientes en la base de datos.
* Manejo de Respuestas:Configura tus controladores para devolver respuestas JSON adecuadas con los datos solicitados o mensajes de error apropiados.
* Utiliza códigos de estado HTTP apropiados (por ejemplo, 200 para respuestas exitosas, 404 para recursos no encontrados, etc.)

# Extras
* Manejo de Excepciones.
* Seguridad y Autenticación.
* Procedimientos almacenados. 
* Documentación de API.
* Responsive Design.
