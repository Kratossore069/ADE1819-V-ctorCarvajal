# Fichero de opciones y variables de servidor.

## 1. Ficheros de opciones.

* Haz la lectura de la siguiente página "Using Option Files" http://dev.mysql.com/doc/refman/5.7/en/option-files.html

* Encuentra el fichero my.ini(en el caso que tu servidor MYSQL estuviera sobre Windows) o my.cnf de tu instalación de MySQL (podría no estar en una ubicación no estándar).

* ¿Cómo se escribe un comentario en este fichero?¿Y un grupo de opciones?¿Todas las opciones tienen un valor?

* Ejecuta "mysqld --verbose --help" desde una consola para ver una lista de las variables del servidor. Para ver mejor el texto mejor redirecciona la salida a fichero.

* Explica qué significan y que se consigue con cada una de las variables del siguiente fichero de configuración.

## 2. Variables del servidor.

* Define qué son las variables del servidor.
* Usa el comando "SHOW VARIABLES" para conocer el valor de todas las variables y enviar el resultado a un fichero (podemos hacerlo desde consola linux y desde el mysql client usando la orden tee.
* Repite lo anterior para mostrar solo las variables relacionadas con el motor "InnoDB".
* Para gestionar variables tenemos, como hemos visto, el comando SHOW "comando":
cómo mostrar todos los motores de almacenamiento
cómo mostrar el estado actual del servidor
cómo averiguar todos los clientes que están conectados al servidor
cómo conocer todas las tablas que están abiertas

## Variables de estado.

* Define qué son las variables de estado.
* Usa el comando "SHOW STATUS" para conocer el valor de todas las variables..
* Haz que uno o más de tus compañeros se conecte a tu servidor (puede que por cuestión de permisos no os podáis conectar).
* Comprueba quién está conectado usando el comando correspondiente (Pista: es un comando visto SHOW XYZ).
* Intenta desconectarlo con el comando "kill"
* ¿Cuántas consultas se están ejecutado hasta el momento en tu servidor MYSQL? ¿Y si se trata de consultas lentas?
* Un estado informa  el sobre el máximo de conexiones concurrentes que se ha dado en la sesión de trabajo. ¿Cuál es?

## Variables dinámicas.

* ¿Cómo podemos saber si una variable es dinámica o no?
* ¿Qué hace la variable "uptime"?
Indica su valor en tu servidor
¿Es posible modificar su valor con comando SET?
* Localiza la variable que establece el límite de conexiones concurrentes. ¿Cuál es? 

Conéctate con tres instancias de la herramienta cliente mysql utilizando un usuario creado previamente (podéis crear el usuario desde WorkBench, es más sencillo).
Comprueba el valor de la variable de estado que indica cuantas conexiones simultáneas fueron establecidas al servidor Mysql (para ello busca la cadena 'connection' en las variables de estado.
Modifica la variable del sistema que limita el número de conexiones simultáneas a 3 (busca que variable es de la misma forma que en el paso anterior).
Piensa: Con que usuario tendrás que ejecutar la orden SQL.
Intenta conectarte con una nueva instancia de Mysql utilizando el usuario creado previamente.
Deja la variable del sistema a su valor por defecto. (se iguala con la palabra DEFAULT)
