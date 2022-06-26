1: se están ejecutando 2 contenedores

2: están basados en las imágenes nicopaez/jobvacancy-ruby:1.3.0 y postgres

3: cada una de las líneas hace lo siguiente:

* version: define el formato del schema que se va a utilizar
* services: define los servicios que se van a correr, cada uno será un container con sus argumentos, en este caso los servicios son web y db
* image: define la imagen desde la cual se inicializa el container
* links: agrega aliases por los cuales se puede acceder a otros servicios
* ports: expone los puertos del contenedor
* environment: define variables de entorno
* depends_on: define una dependencia en el orden de inicio y apagado entre los servicios

4: los contenedores pueden verse entre sí porque compose crea una red por defecto y cada container creado se va uniendo a dicha red
