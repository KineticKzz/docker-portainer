# INSTALACION DOCKER PORTAINER GNU/LINUX
## INSTALACION
- Primero vamos a crear un volumen

        docker volume create docker-portainer

- Ahora vamos a crear el contenedor.

        docker run -d -p 8080:8080 -v /var/run/docker.sock:/var/run/docker.sock -v docker-portainer:/data portainer/portainer

Usaremos la imagen de portainer/portainer

Necesitamos que esté la conexion de /var/run/docker.sock para que haya conectividad entre nuestro equipo y los contenedores que creemos en portainer.io

Por último hemos compartido nuestro volumen creado en local con la carpeta /data de nuestro contenedor

        


## CONFIGURACION
