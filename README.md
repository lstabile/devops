# Devops

[Wiki](https://github.com/lstabile/devops/wiki)

# Comandos útiles

## Docker 

| Comando | Descripción |
|:--------|:------------|
| `docker pull sotobotero/udemy-devops:0.0.1` | descargar una imagen |
| `docker image ls` | listar imágenes |
| `docker rmi $(docker images -a -q)` | eliminar todas las imágenes |
| `docker ps -a` | listar contenedores |
| `docker system prune` | eliminar todos los contenedores detenidos |
| `docker stop $(docker ps -a -q)` | detener todos los contenedores |
| `docker volume ls` | listar todos los volumenes |
| `docker volume prune` | eliminar todos los volumenes |
| `docker network ls` | listar las redes virtuales |
| `docker network create NETWORK_NAME` | crear una red virtual con el nombre especificado |
| `docker network connect NETWORK_NAME CONTAINER_NAME` | conectar el contenedor CONTAINER_NAME a la red virtual NETWORK_NAME |
| `docker network prune` | eliminar las redes virtuales |
| `docker run -d -p 81:80 docker/getting-started` | instanciar el contenedor getting-started como demonio en el puerto 81 y traducirlo al 80 |
| `docker start CONTAINER_ID` | Iniciar el contenedor con el ID indicado (puede ser el nombre también) |
| `docker logs CONTAINER_ID ` | Ver logs del contenedor con el ID indicado (puede ser el nombre también) |
| `docker stop CONTAINER_ID ` | Detener la ejecución de un contenedor (puede ser el nombre también) |
| `docker rm CONTAINER_ID` | eliminar el contenedor con el ID indicado (puede ser el nombre también) |
| `docker image rm IMAGE_ID` | eliminar la imagen con el ID indicado |
| `docker tag IMAGE_ID:TAG NEW_IMAGE_ID:NEW_TAG` | renombrar una imagen local |
| `docker login` | loguearnos desde consola a docker hub |
| `docker push IMAGE_ID:TAG` | subir la imagen IMAGE_ID:TAG a docker hub |
| `docker stats` | ver los recursos asignados a cada contenedor |
| `docker container inspect CONTAINER_NAME` | mostrar los detalles del contenedor CONTAINER_NAME |

## Docker compose

| Comando | Descripción |
|:--------|:------------|
| `docker compose -f FILENAME.yml build` | construir las imágenes definidas en la orquestación |
| `docker compose -f FILENAME.yml up -d` | inicializar los contenedores de los servicios de la orquestación |
| `docker compose -f FILENAME.yml stop` | detener todos los servicios definidos en la orquestación |
| `docker-compose -f FILENAME.yml build --no-cache` | reconstruir las imágenes |
| `docker-compose -f FILENAME.yml up -d --force-recreate` | reconstruir los contenedores de la orquestación |


## Minikube

| Comando | Descripción |
|:--------|:------------|
| `minikube start` | iniciar el cluster. Levanta el contenedor de minikube en docker |
| `minikube stop` | detener el contenedor de minikube |
| `minikube status` | mostrar el estado del contenedor de minikube |
| `minikube delete` | eliminar el cluster de minikube |
| `minikube dashboard` | levantar el sitio web de minikube dashboard |
| `minikube service list` | listar los servicios disponibles del cluster |
| `minikube service NAME` | abrir una solicitud para el servicio con nombre `NAME` |
| `minikube config set cpus 2` | configurar el límite de cpu en 2 |
| `minikube config set memory 2g` | configurar el límite de memoria a 2 gigas |

## Kubernetes
| Comando | Descripción |
|:--------|:------------|
| `kubectl run NOMBRE_POD --image=NOMBRE_IMG --port=PORT PORT` | crea un pod y lo ejecuta |
| `kubectl get pods` | listar los pods |
| `kubectl describe pod NOMBRE_POD` | mostrar la información del pod |
| `kubectl delete pod NOMBRE_POD` | eliminar un pod |
| `kubectl expose pod NOMBRE_POD --type=LoadBalancer --port=EXTERNAL_PORT --target-port=INTERNAL_PORT` | exponer un servicio asociado al pod indicado |
| `kubectl get services` | listar los servicios |
| `kubectl describe services NOMBRE_SERVICE` | mostrar la información del servicio NOMBRE_SERVICE |
| `kubectl delete service NOMBRE_SERVICE` | eliminar el servicio |
| `kubectl apply -f FILENAME.yml` | aplicar la configuración indicada en el archivo FILENAME |
| `kubectl get all` | mostrar un resumen de los objetos ejecutándose en el cluster |
| `kubectl apply -f ./` | levantar todos los objetos según la configuraciones del directorio actual |
| `kubectl delete -f ./` | bajar todos los objetos cuyo archivo de configuración está en el directorio actual |


