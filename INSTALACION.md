# INSTALACION DOCKER PORTAINER GNU/LINUX
## INSTALACION
- Primero vamos a crear un volumen

        docker volume create docker-portainer

- Ahora vamos a crear el contenedor.

        docker run -d -p 8080:9000 -v /var/run/docker.sock:/var/run/docker.sock -v docker-portainer:/data portainer/portainer

Usaremos la imagen de portainer/portainer. El puerto por defecto de portainer.io es el 9000, pero a mi me gusta mas el 8080 asi que lo redirecciono localmente

Necesitamos que esté la conexion de /var/run/docker.sock para que haya conectividad entre nuestro equipo y los contenedores que creemos en portainer.io

Por último hemos compartido nuestro volumen creado en local con la carpeta /data de nuestro contenedor

        


## CONFIGURACION
Una vez seguido los pasos anteriores, nos dirigiremos al navegador y accederemos a localhost:puerto. En mi caso será lo siguiente

        http://localhost:8080
        
Y nos deberá de aparecer una imagen como la siguiente. Creamos un usuario y la contraseña y estamos dentro

![img](https://i.imgur.com/ikNZu3W.png)
