# DOCKER

## Construir imagenes
Docker nos permite crear imagenes desde cero o poder utilizar alguna imagen ya creada desde su [repositorio de imagenes.](https://hub.docker.com/search?q=&type=image) 

En el repositorio de dockerhub podemos encontrar muchas imagenes creadas por diferentes usuarios, sin embargo, dockerhub nos añade una etiqueta en el cual podemos saber si la imagen es oficial o no, esto debido a que cualquier usuario puede crear imagenes, incluso nosotros mismos podemos tener imagenes públicas que utilicemos frecuentemente o simplemente por alguna necesidad de algún proyecto.

## Comandos básicos
Consultar las imagenes disponibles
```bash
$docker images
```
Consultar los contenedores activos

```bash
$docker ps
```
Consultar los contenedores disponibles (activos y no activos)
```bash
$docker ps -a
```
Cómo eliminar contenedoresbash
```
$docker rm <CONTAINER_NAME>
$docker rm <CONTAINER_ID>
```
Cómo eliminar imagenes
```bash
$docker rm <IMAGE_NAME:TAG>
$docker rm <IMAGE_ID>
```
Levantar un contenedor
```bash
$docker start <CONTAINER_ID>
$docker start <CONTAINER_NAMES>
```
Bajar un contenedor
```bash
$docker stop <CONTAINER_ID>
$docker stop <CONTAINER_NAMES>
```
Poda del sistema Docker
```bash
$docker system prune [OPTIONS]
```
Dentro de las opciones tenemos:

| NOMBRE, ABREVIATURA	| DESCRIPCIÓN |
| ---------------------| --------------|
| all, -a	            | Elimine todas las imagenes no utilizadas|
| filter	            | Proporcione valores para el filtro (ejemplo label==) |
| force, -f           | No pedir confirmación |
| volumes	            | Podar volúmenes |

Descargar imagenes desde dockerhub
Para descargar imagenes creadas tenemos que ejecutar el comando docker pull, por ejemplo, descargar la imagen de un sistema operativo ubuntu:
```bash
$docker pull ubuntu
```
Sin embargo, si no le definimos un tag, por defecto viene el latest (la última version subida al dockerhub). Como una buena práctica se recomienda definir el tag que estamos utilizando, siguiendo el ejemplo anterior, quiero obtener una imagen de ubuntu versión 20.04:
```bash
$docker pull ubuntu:20.04
```
Crear ambiente para correr R en jupyter-notebook (para más detalle podemos ver un ejemplo)
```bash
$docker pull jupyter/r-notebook:r-4.2.2
$docker run -it -p 8888:8888 --name r-container jupyter/r-notebook:r-4.2.2
```
Crear ambiente para correr R en jupyter-notebook que contenga Tensorflow y Keras (para más detalle podemos ver un ejemplo)
```bash
$docker pull kaggle/rstats
$docker run -it -p 8085:8085 --name r-container kaggle/rstats
```

