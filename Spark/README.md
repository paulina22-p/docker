# DOCKER - SPARK

Se descarga la imagen de `pyspark-notebook`, la cual permite crear contenedores con todas las configuraciones necesarias para ejecutar código PySpark en la versión 3.4.1 de Spark.

## Pasos de configuración

1. Clonar el repositorio:
   ```bash
   git clone https://github.com/paulina22-p/docker.git
2. Cambiarse de carpeta al servidor que queremos instalar SQL Server:  
   ```bash
    cd docker/Spark
3. Ejecutar el comando para la descarga de la imagen y configuración del contenedor:
   ```bash
    docker-compose up
   
### Una vez creado el contenedor
Si se requiere levantar nuevamente el contenedor, existen dos maneras:  
**Opción 1:** 
  ```bash
     docker-compose up
  ```

**Opción 2:**
  ```bash
     docker start pyspark_container
```

##Acceso a Jupyter Notebook
### Una vez levantado el contenedor y no se logra identificar el token para acceder al Jupyter notebook se requiere seguir los siguientes pasos:  
1. Entrar al contendor:
      `winpty docker exec -it pyspark_container sh`  
2. Ejecutar el comando para listar los servidores de Jupyter
      `jupyter server list`  
3. En la URL del navegador escribir:
      `http://localhost:8888/lab`  
#### En caso de requerir el Token con el comando anterior se puede extraer.
Si se requiere apagar el contenedor puedes detener Docker o bien ejecutar el comando para apagar solo el contenedor que contiene la aplicación de Spark.
```bash 
  docker stop pyspark_container

