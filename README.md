https://github.com/oracle/docker-images/tree/main/OracleDatabase/SingleInstance

chmod u+x buildContainerImage.sh

./buildContainerImage.sh -v 11.2.0.2 -t oracle-xe -x -i
