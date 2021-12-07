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
