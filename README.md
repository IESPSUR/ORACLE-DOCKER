# ORACLE PARA DOCKER

REFERENCIA DOCUMENTACIÓN OFICIAL
https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance

## INSTRUCCIONES GENERALES

1. Necesitas cumplir los requisitos previos
2. Construir la imagen del contenedor ORACLE que vayas a usar
3. Crear y usar contenedor ORACLE

## REQUISITOS PREVIOS

Instalar:
1. docker
2. docker-compose

## CONSTRUCCIÓN DE IMÁGENES

Antes de poder crear tu contenedor de base de datos tiene que existir una imagen
en tu repositorio local de docker images
```
$ docker images
REPOSITORY        TAG         IMAGE ID       CREATED         SIZE
oracle-database   11.2.0-XE   98da15b6c229   4 minutes ago   1.15GB
oraclelinux       7-slim      5fe1636f17bb   33 hours ago    132MB
```

Para crear las imágenes como se ha mostrado en el ejemplo anterior sigue las instrucciones para cada versión

### CONSTRUIR IMAGEN PARA ORACLE 11.0.2 EXPRESS
Descargar binarios de Docker Express 11 en carpeta 11.2.0.2  
https://drive.google.com/open?id=11sTooKthWuSnDLeRYlc_F05PCVlwdE1y&authuser=0

Construir docker image  
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 11.2.0.2 -t oracle-database:11.2.0-XE -x -i
```

### CONSTRUIR IMAGEN PARA ORACLE 18.4.0 EXPRESS EDITION  

Descargar binarios de ORACLE DATABASE 18.4.0 en carpeta 18.4.0
https://drive.google.com/file/d/1StCsG2DSnvWGOPRj0ROphjm9fSpKk1Up/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 18.4.0 -t oracle-database:18.4.0-XE -x -i
```

### CONSTRUIR IMAGEN PARA ORACLE 19.3.0 STANDARD EDITION  

Descargar binarios de ORACLE DATABASE 19.3.0 en carpeta 19.3.0
https://drive.google.com/file/d/1Li62iexlLNA-sSZ1Jx6luGFtLHq1cKTf/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 19.3.0 -t oracle-database:19.3.0-SE -s -i
```

### CONSTRUIR IMAGEN PARA ORACLE 19.3.0 ENTERPRISE EDITION

Descargar binarios de ORACLE DATABASE 19.3.0 en carpeta 19.3.0
https://drive.google.com/file/d/1Li62iexlLNA-sSZ1Jx6luGFtLHq1cKTf/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 19.3.0 -t oracle-database:19.3.0-EE -e -i
```

### RESOLUCIÓN ERRORES AL CREAR IMÁGENES

Las imagenes dependen de otra imagen oraclelinux que se crea conjuntamente. En caso de error borrar todas las imágenes que puedan interferir antes de construir.

## CREACIÓN DE CONTENEDORES Y USO

1. Sitúate en la carpeta en la que tengas el docker-compose.yml
2. Copia el fichero de la version a utilizar al fichero docker-compose.yml
3. Crear contenedor `docker-compose up -d`
4. Consultar si ha arrancado  `docker-compose logs`
5. Esperar al mensaje  
```
#########################  
DATABASE IS READY TO USE!  
#########################
```

Ya puedes conectar por el puerto 1521

## INFORMACIÓN ADICIONAL

Con un poco de conocimiento de docker se pueden conseguir fácilmente muchas funciones adicionales que se encuentran en la documentación oficial referenciada al inicio de este documento. Por ejemplo:
1. [Ejecución automática de scripts](https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance#running-scripts-after-setup-and-on-startup) tras la creación del contenedor
2. Montar volúmenes para mantener persistencia de la bd aún cuando se borra o recrea el contenedor
