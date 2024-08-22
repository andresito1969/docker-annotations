# Primeros pasos
docker pull hello-world // obtiene la imagen hello-world del repositorio -> https://hub.docker.com/_/hello-world (al no haber especificado nada, la obtiene de ese repo)

docker container run -d -p 80:80 hello-world // con la imagen obtenida, creamos y corremos un contenedor
// El parámetro {-d}  nos permite hacer un detach en la consola, es decir que nos permita seguir usándola y no quede parada
// El parámetro {-p 80:80} nos permite publicar el contenedor en el puerto 80, con lo cual al hacer localhost vemos esa imagen, **el primer 80 equivale a nuestro puerto, el segundo al puerto expuesto por esa imagen**

docker {container || image} help

docker {container || image} ls -a // Permite obtener todos los contenedores o imagenes que tenemos

docker {container || image} prune // Permite borrar los contenedores o imagenes que no estemos usando

docker {container || image} rm {id} // Permite borrar un o varios contenedores o imagenes pasándole el id (podemos pasar los 3 primeros carácteres y funcionaría igual)

docker container stop {id} // Permite parar un contenedor al que se ha hecho detach
docker container start {id} // Reanuda el contenedor parado

