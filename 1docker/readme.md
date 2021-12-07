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