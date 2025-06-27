##Docker - Spark  
Se descarga la imagen de pyspark-notebook, la que nos permite crear contenedores con todas las configuraciones necesarias para ejecutar código Pyspark en la versión 3.4.1 de Spark.  
Para configurar esto se debe clonar el repositorio:  
`git clone https://github.com/paulina22-p/docker.git`  
Cambiarse de carpeta al servidor que queremos instalar SQL Server:  
`cd docker/Spark`  
Ejecutar el comando para la descarga de la imagen y configuración del contenedor:
`docker-compose up`  
###Una vez creado el contenedor y si se requiere levantar el contenedor existen dos maneras:
--Opción 1: `docker-compose up`
--Opción 2: `docker start pyspark_container`  
Una vez levantado el contenedor y no se logra identificar el token para acceder al Jupyter notebook se requiere seguir los siguientes pasos:


