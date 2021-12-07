### Crear fichero de dockerfile


---

### crear imagen en la ruta donde esta el docker file esta va sin el nombre y la version
* `docker build .`

### listar imagenes

* `docker images`

### Eliminar imagen se coloca el id de la imagen

* `docker image rm 32c5397c4387`

### crear imagen con la etiqueta y version
* `docker build -t imagen:1.0 .`

### cambiar nombre de la imagen y la etiqueta
* `docker tag imagen:1.0 helloworld:latest`

### ver metadatos e inspeccionar 
* `docker inspect 90121a78b9bb` <= el id o el nombre de la imagen mas el tag

---

### crear contenedor 
* `docker create 90121a78b9bb` <== puede ser el nombre de la imagen o el id

### ver los que estan en ejecucion
* `docker ps`

### ver los que estan parados
* `docker ps -a`

### eliminar contenedor
* `docker rm id`

### correr docker
* `docker start id_container`

### deterner container

* `docker stop 59d9f7a1d3b8`

### eliminar container cuando esta corriendo
* `docker rm aea8080ded60 -f`

### crear container con el nombre personalizado
* `docker create --name web1 helloworld`

---

### obtener ip con docker inspect id_container y lanzar en el navegador

### crear contenedor con el puerto :80
* `docker create -p 8080:80 --name web1 helloworld`

### colocar ip de la maquina o ell localhost:8080

## reetiquetar
* `docker tag hello:20.0 hello:latest`

### Crear contenedor con puertos expuestos
* `docker create -P --name web1 hello`

### se crea y se pone en ejecucion
* `docker run -d -P --name web2 hello`

---

### troubleshoting

###### Lista 
* `docker exec web1 ls`

##### procesos
* `docker exce web1 ps`

##### ejecutar bash entra al contenedor
* `docker exex -it web1 bash`

##### ver los logs va despues de haber entrado^
* `taill -f /var/log/nginx/access.log`

---
## volumenes persistentes

###### Listar volumenes
* `docker volume ls`

##### crear volumen
* `docker volume create my-volume`

##### ver propiedades del volumen
* `docker volume inspect my-volume`

##### crear container en el volumen creado
* `docker create -P --mount source=my-volume,target=/var/www/html --name web2 hello`
##### Listar la data del volumne creado
* `sudo ls /var/lib/docker/volumes/my-volume/_data`

---

## Network

#### Lista de redes
* `docker network ls`

#### crear red

* `docker network create web1 --driver bridge`

#### Info de la red
* `docker network inspect web2`

### crear contenedor en la red creada
* `docker run -P -d --name web1a --network web1 hello`

### entrar a un contenedor
* `docker exec -it web1a bash`

### eliminar subredes
* `docker network prune`

### conectar una red al contenedor
* `docker network connect nombre_Red nombre_container`

### docker hub
#### tag de la imagen local debe ir el nombre de usuario del docker hub `https://hub.docker.com/`
* `docker tag hello jdvpl/hello`
#### subir imagen

* `docker push jdvpl/hello`

### bajar imagen 
* `docker pull jdvpl/hello`





