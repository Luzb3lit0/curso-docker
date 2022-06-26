HEALTHCHECK: tiene 2 formas diferentes. 

* HEALTHCHECK [OPTIONS] CMD command
* HEALTHCHECK NONE

El segundo deshabilita los HEALTCHECKs heredados de la imagen base.

El primero sirve para ver el estado del contenedor. Se agrega un health status además de su status de siempre. El comando que se ejecuta en el HEALTCHECK determina si el contenedor es healthy o unhealthy. Solo puede haber un HEALTCHECK por Dockerfile.


ONBUILD: se utiliza para correr instrucciones que tienen que correrse en el build pero son especificadas en una imagen base. Cuando se crea un nuevo build con esta imagen como base, se ejecutan todas las instrucciones ONBUILD en el orden que aparecieron a continuación del FROM y si alguna de estas falla se aborta el FROM. Los ONBUILD no son heredados por los nietos de la imagen base.


VOLUME: crea un volumen que es agnóstico al host del container, dichos volúmenes se crean en la máquina host con un id al azar dentro de /var/lib/docker/volumes/ y pueden ser compartidos por distintos contenedores.
