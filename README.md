# ORACLE PARA DOCKER

REFERENCIA OFICIAL
https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance

## VERSIÓN 11.0.2 EXPRESS
Descargar binarios de Docker Express 11 en carpeta 11.2.0.2  
https://drive.google.com/open?id=11sTooKthWuSnDLeRYlc_F05PCVlwdE1y&authuser=0

Construir docker image  
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 11.2.0.2 -t oracle-database:11.2.0-XE -x -i
```

Usar docker-compose  
`docker-compose up -d`

Consultar si ha arrancado  
`docker-compose logs`

Esperar al mensaje  
```
#########################  
DATABASE IS READY TO USE!  
#########################
```

## VERSIÓN 18.4.0 EXPRESS EDITION  

Descargar binarios de ORACLE DATABASE 18.4.0 en carpeta 18.4.0
https://drive.google.com/file/d/1StCsG2DSnvWGOPRj0ROphjm9fSpKk1Up/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 18.4.0 -t oracle-database:18.4.0-XE -x -i
```

Usar docker-compose
`docker-compose up -d`

Consultar si ha arrancado
`docker-compose logs`

Esperar al mensaje
```
#########################
DATABASE IS READY TO USE!
#########################
```


## VERSIÓN 19.3.0 STANDARD EDITION  

Descargar binarios de ORACLE DATABASE 19.3.0 en carpeta 19.3.0
https://drive.google.com/file/d/1Li62iexlLNA-sSZ1Jx6luGFtLHq1cKTf/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 19.3.0 -t oracle-database:19.3.0-SE -s -i
```

Usar docker-compose
`docker-compose up -d`

Consultar si ha arrancado
`docker-compose logs`

Esperar al mensaje
```
#########################
DATABASE IS READY TO USE!
#########################
```

## VERSIÓN 19.3.0 ENTERPRISE EDITION

Descargar binarios de ORACLE DATABASE 19.3.0 en carpeta 19.3.0
https://drive.google.com/file/d/1Li62iexlLNA-sSZ1Jx6luGFtLHq1cKTf/view?usp=sharing

Construir docker image
```
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 19.3.0 -t oracle-database:19.3.0-EE -e -i
```

Usar docker-compose
`docker-compose up -d`

Consultar si ha arrancado
`docker-compose logs`

Esperar al mensaje
```
#########################
DATABASE IS READY TO USE!
#########################
```


