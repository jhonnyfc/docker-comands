# docker-comands

### Descargar la imagen deseada de DockerHub
````
$ docker pull imageName:version
````

### Para ver las imagenes que estan descargadas en el pc
````
$ docker images
````

### Ejecutar la imagen deseada, te la descarga si no la tienes
````
$ dokcer run imageName
````

### Se ejecuta sin salida de logs por terminal y printea el id
````
$ docker run -d imageName
````

### Se para el conendor con el id dado
````
$ docker stop idContenedor 
````

### Se ejecuta el conendor con el id dado
````
$ docker start idContenedor
````

### Lista los contenedores que se estan ejecutando
````
$ docker ps
````

### Lista los contenedores se esten ejecutando o no
````
$ docker ps -a
````

### Hace un mapeo de el puerto del contenedor al puerto del pc
````
$ docker run -p:portPc:portContainer idContenedor || imageName 
````

### Da nombre al contenedor que va ejecutar la imagen, para que no haga falta recordar el id
````
$ docker run --name myContName imageName
````

### Muestra los losgs de contenedor
````
$ docker logs idContenedor || myContName
````

### Muestra los ultimos losgs de contenedor
````
$ docker logs idContendor | tail
````

### Abre un interactive terminal para el contenedro deseado
````
$ docker exec -it idContenedor || myContName /bin/bash || /bin/sh
````

### Muestra las redes que tiene docker por defecto y las que has añadido
````
$ docker network ls
````

### Crea un nueva red
````
$ docker network create netName
````

### Ejectua un Contenerod y le asociamos una red docker
````
$ docker run --net netName myContName
````

### Ejectua los contnedores que se han configurado en el .yaml
````
$ docker-compose -f fileName.yaml up
````

### Ejectua los contnedores que se han configurado en el .yaml sin salida por terminal
````
$ docker-compose -d -f fileName.yaml up
````

### Termina la ejecucion del archivo .yaml y sus contenedores
````
$ docker-compose -f fileName.yaml down
````

### A partir de un Docker file creamos una imagen con un nombredado, si esta en el mismo dir no hace falta dar la ruta del Docker file
````
$ docker build -t myAppName:Num.version.name
````

### Borra una imagen
````
$ docker rmi imageName || idimage
````

### Borra una contenedor
````
$ docker rm myContName || idContendor
````

### Aspcoa un id para subir la imagen a otro repo que no sea docker hub
````
$ docker tag myAppName:image añadimoseURLTAgPArPoderSubirLaImagen
````

### Crea un volumen para persitir los datos de un contenedor
````
$ docker run -v dirhodt:path/dockercont
````