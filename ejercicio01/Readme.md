Para correr el ejercicio ejecutar los siguientes comandos:

docker build -t ejercicio01-nginx .
docker run --name ejercicio01 -d -p 8080:80 ejercicio01-nginx
