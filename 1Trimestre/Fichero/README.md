# Fichero de opciones y variables de servidor.

## 1. Ficheros de opciones.

* Haz la lectura de la siguiente página "Using Option Files" http://dev.mysql.com/doc/refman/5.7/en/option-files.html

* **Encuentra el fichero my.ini(en el caso que tu servidor MYSQL estuviera sobre Windows) o my.cnf de tu instalación de MySQL (podría no estar en una ubicación no estándar).**

![](./img/img1.PNG)

* **¿Cómo se escribe un comentario en este fichero?¿Y un grupo de opciones?¿Todas las opciones tienen un valor?**

*Los comentarios se escriben: = [a partir de aquí se escribe y] # para finalizar el comentario. Un grupo de opciones se escriben de la siguiente manera: Grupo = [Caracteres]. No todas las opciones tienen un valor.*

* **Ejecuta "mysqld --verbose --help" desde una consola para ver una lista de las variables del servidor. Para ver mejor el texto mejor redirecciona la salida a fichero.**

![](./img/img2.PNG)

![](./img/img3.PNG)

* **Explica qué significan y que se consigue con cada una de las variables del siguiente fichero de configuración.**

* [client]
* port=3306 => *Es el puerto de escucha.*
* password="telesforo"; => *Contraseña de inicio del cliente*.

* [mysqld]
* port=3306 => *Otro puerto de escucha de la información*.
* key_buffer_size=16M => *Tamaño máximo de memoria de 16 Mb.*
* max_allowed_packet=8M => *Tamaño máximo de paquetes de 8 Mb.*
* [mysqldump]
* quick => *Significa que la copia de seguridad se ejecutará de manera rápida cuando esté utilizando mysqldump*.

## 2. Variables del servidor.

* **Define qué son las variables del servidor.**

*Las variables de Servidor almacenan información relativa al entorno de ejecución de una aplicación ASP. Una de las aplicaciones más utilizadas de estas variables es la obtención del identificador de usuario.*

* **Usa el comando "SHOW VARIABLES" para conocer el valor de todas las variables y enviar el resultado a un fichero (podemos hacerlo desde consola linux y desde el mysql client usando la orden tee.**

![](./img/img4.PNG)

* **Repite lo anterior para mostrar solo las variables relacionadas con el motor "InnoDB".**

![](./img/img5.PNG)

* **Para gestionar variables tenemos, como hemos visto, el comando SHOW "comando":**
* cómo mostrar todos los motores de almacenamiento

![](./img/img6.PNG)

* cómo mostrar el estado actual del servidor

![](./img/img7.PNG)

* cómo averiguar todos los clientes que están conectados al servidor

![](./img/img8.PNG)

* cómo conocer todas las tablas que están abiertas

![](./img/img9.PNG)

## Variables de estado.

* **Define qué son las variables de estado.**

*Una variable de  estado es por ejemplo el número el número de segundos que el servidor está arrancado, el número de estados también es dependiente de la versión más de 300 para la vesión 5.5.*

* **Usa el comando "SHOW STATUS" para conocer el valor de todas las variables..**

![](./img/img10.PNG)

* **Haz que uno o más de tus compañeros se conecte a tu servidor (puede que por cuestión de permisos no os podáis conectar).**

![](./img/img11.PNG)

* **Comprueba quién está conectado usando el comando correspondiente (Pista: es un comando visto SHOW XYZ).**

![](./img/img12.PNG)

* **Intenta desconectarlo con el comando "kill"**.

![](./img/img13.PNG)

* **¿Cuántas consultas se están ejecutado hasta el momento en tu servidor MYSQL? ¿Y si se trata de consultas lentas?**

![](./img/img14.PNG)

* **Un estado informa  el sobre el máximo de conexiones concurrentes que se ha dado en la sesión de trabajo. ¿Cuál es?**

![](./img/img15.PNG)

## Variables dinámicas.

* **Detalla los posibles atributos que tendría una variable de servidor como "port".**

Command-Line Format

System Variable

Name: port

Variable Scope: Global

Dynamic Variable: No

Permitted Values

Type: integer

Default: 3306

Min Value: 0

Max Value: 65535

* **¿Cómo podemos saber si una variable es dinámica o no?**

*Las variables que se pueden observar con show variables son dinamicas y las que se muestran show status son fijas.*

* **¿Qué hace la variable "uptime"?**

*Muestra el tiempo que lleva activo el servidor desde su último reinicio o puesta a 0.*

* **Indica su valor en tu servidor**

![](./img/img16.PNG)

* **¿Es posible modificar su valor con comando SET?**

*No, porque no es una varaible dinámica.*

* **Localiza la variable que establece el límite de conexiones concurrentes. ¿Cuál es?**

![](./img/img17.PNG)

* **Conéctate con tres instancias de la herramienta cliente mysql utilizando un usuario creado previamente (podéis crear el usuario desde WorkBench, es más sencillo).**

![](./img/img18.PNG)

![](./img/img19.PNG)

* **Comprueba el valor de la variable de estado que indica cuantas conexiones simultáneas fueron establecidas al servidor Mysql (para ello busca la cadena 'connection' en las variables de estado.**

![](./img/img20.PNG)

* **Modifica la variable del sistema que limita el número de conexiones simultáneas a 3 (busca que variable es de la misma forma que en el paso anterior).
Piensa: Con que usuario tendrás que ejecutar la orden SQL.**

![](./img/img21.PNG)

* **Intenta conectarte con una nueva instancia de Mysql utilizando el usuario creado previamente.**

![](./img/img22.PNG)

* **Deja la variable del sistema a su valor por defecto. (se iguala con la palabra DEFAULT)**

![](./img/img23.PNG)
