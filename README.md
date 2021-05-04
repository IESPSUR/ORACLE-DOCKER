https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance

Descargar binarios de Docker Express 11 en carpeta 11.2.0.2  
https://drive.google.com/open?id=11sTooKthWuSnDLeRYlc_F05PCVlwdE1y&authuser=0

Construir docker image  
chmod u+x buildContainerImage.sh
./buildContainerImage.sh -v 11.2.0.2 -t oracle-xe -x -i

Usar docker-compose  
docker-compose up -d

Consultar si ha arrancado  
docker-compose logs

Esperar al mensaje  
` #########################  
 DATABASE IS READY TO USE!  
 #########################`
