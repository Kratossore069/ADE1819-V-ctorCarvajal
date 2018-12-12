# Privilegios y creación de usuarios.

![](./img/1.PNG)

![](./img/2.PNG)

![](./img/3.PNG)

grant select on `*.*`

grant select on jardineria.Empleados to alumno;

flush privileges;

create user alumno@'172.19.14.11' identified by '123';

![](./img/4.PNG)

Modifica el host desde donde pueda acceder el alumno a una dirección IP determinada (del propio servidor o un cliente). Soluciona los problemas que pueda presentar esta modificación.

![](./img/5.PNG)

> Si se quiere volver a dejar como estaba: `bind-address = *`

![](./img/6.PNG)

![](./img/7.PNG)

![](./img/8.PNG)

![](./img/9.PNG)

![](./img/10.PNG)

![](./img/11.PNG)

create view "NOMBRE" as "CONSULTA";

![](./img/12.PNG)

![](./img/13.PNG)

update "TABLA" set "LQUESEA"where "LOQUESEA";

![](./img/14.PNG)
