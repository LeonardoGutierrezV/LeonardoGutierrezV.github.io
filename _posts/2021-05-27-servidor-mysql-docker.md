---
layout: single
title: Montar un servidor MySQL en Docker
excerpt: "Vamos a montar un servidor MySQL utilizando un contenedor Docker y conectarnos al mismo, mediante una terminal y MySQL Workbench. "
date: 2021-05-27
classes: guía
header:
  teaser: /assets/images/ /servidor-mysql-docker/logo.png
  teaser_home_page: true
  icon: /assets/images/db_icon.png
categories:
  - MySQL
  - Docker
  - Windows
tags:
  - MySQL
  - Base de datos
  - Docker
  - Windows
---
![](/assets/badges/mysql.svg) ![](/assets/badges/docker.svg) ![](/assets/badges/windows.svg)

Una vez que tengamos instalado Docker en nuestro equipo, debemos crear una carpeta de trabajo para el contenedor y todos los archivos relacionados el proyecto, sobre todo si además de usar contenedores pretendemos agregar esto a un repositorio de trabajo.

Para comenzar necesitaremos crear un archivo de configuración con extensión **.yml**, que permita al contenedor crearse con los parámetros que necesitamos. Es necesario tener en cuenta que estos archivos son versionados y, que de acuerdo con la versión indicada en el encabezado los comandos insertados en el cuerpo del archivo van a variar. 


```yaml
version: '3.3'
services:
  db:
    container_name: 'mycontainer'
    image: mysql:8.0
    environment:
      MYSQL_DATABASE: 'Prototipo'
      MYSQL_USER: 'leonardo'
      MYSQL_PASSWORD: '098765'
      MYSQL_ROOT_PASSWORD: '12345'
      # Permitir la conexion remota al servicio
      MYSQL_ROOT_HOST: '%'
    ports:
      # Configuración de puerto
      - '3306:3306'
      # Configuracion de datos persistentes
    volumes:
    - ./sql-data/db:/var/lib/mysql
```

Una vez creado el archivo de configuración del contenedor y haberlo guardado en nuestro directorio de trabajo con el nombre **docker-compose.yml**. Debemos abrir el **CMD**. O dirigirnos a la carpeta de trabajo y ejecutar **Git Bash** si tenemos Git instalado. En nuestra terminal y una vez que nos encontramos en ele directorio de trabajo hay que teclear el siguiente comando.

```bash
docker-compose u -d
```
De acuerdo con la configuración de nuestro archivo y las capacidades de nuestro equipo el montaje del container puede tardar un par de minutos, pero una vez que se encuentre montado, la terminal nos mostrara la siguiente leyenda.

```bash
Network dockerservidormysql_default  Creating
Network dockerservidormysql_default  Created
Container mycontainer  Creating
Container mycontainer  Created
Container mycontainer  Starting
Container mycontainer  Started
```

Algo importante para tener en cuenta es que al agregar -d a nuestro comando estamos lanzando el contenedor de forma desatendida, por lo que únicamente nos indicara cuando el contenedor este listo, debemos darle un par de minutos al servidor para que inicialice el servicio de MySQL.

La carpeta en la que se encuentra nuestro archivo compose y donde se ejecuto el comando indicado, ahora contendrá una carpeta con los datos persistentes de la base de datos. y nuestro servidor ahora es funcional.

![](/assets/images/servidor-mysql-docker/sql-data.png)

Por omisión el contenedor tomara una dirección IP **127.0.0.1**, de tal manera que podemos conectarnos al servicio sin problemas. 

## Conexion mediante Workbench

Asumiendo que tenemos **MySQL Workbench** instalado, debemos abrirlo y nos dirigimos al mebu **Database>Connect to Database** o presionamos las teclas **Ctrl+U** para abrir la ventana de conexion a base de datos.

![](/assets/images/servidor-mysql-docker/connection.png)

Por omisión **Workbench** busca la dirección IP default del servidor MySQL, así que solo debemos dar clic en el botón *OK* y se nos mostrara la ventana de acceso.

![](/assets/images/servidor-mysql-docker/loggin.png)

Solo será necesario proporcionar la contraseña registrada en el archivo **docker-compose.yml**.

Si todo ha ido bien entonces se abrirá la **Workbench** conectado al servicio de **MySQL** en nuestro contenedor para poder trabajar.

![](/assets/images/servidor-mysql-docker/workbench.png)

## Conexion mediante CMD

Tenemos la alternativa de acceder de manera directa al bash de servidor desde una ventana de CMD de Windows para efectos de poder trabajar en la configuración del propio servidor.
Para ello solo tenemos que presionar las teclas **Win+R** para lanzar la ventaja **Ejecutar**.

![](/assets/images/genericos/wejecutar.png)

En esta ventana debemos escribir el siguiente comando.

```bash
cmd /k docker exec -it mycontainer /bin/bash -l
```
Después de presionar la tecla **enter** o dar clic en el botón **Aceptar** se nos desplegara una ventana de comandos de **Windows** similar a la siguiente-

![](/assets/images/servidor-mysql-docker/mysqlcmd.png)

En este punto ya nos encontramos dentro del servidor que contiene el servicio de MySQL, entonces debemos acceder al servicio de la manera en que se haría normalmente en terminal de comandos.

```bash
 mysql -u root -p
 ```

 Si los datos de inicio de sesión son correctos deberíamos recibir el mensaje de MySQL indicando que podemos comenzar a trabajar.

 ```bash
Welcome to the MySQL monitor.  Commands end with ; or \g.
Your MySQL connection id is 16
Server version: 8.0.28 MySQL Community Server - GPL

Copyright (c) 2000, 2022, Oracle and/or its affiliates.

Oracle is a registered trademark of Oracle Corporation and/or its
affiliates. Other names may be trademarks of their respective
owners.

Type 'help;' or '\h' for help. Type '\c' to clear the current 
input statement.

mysql>
 ```

Lo que hay que tener presente al momento de utilizar contenedores inicializados por archivos compose, es la versión que se estará utilizando para evitar problemas con la generación y ejecución de los contenedores.