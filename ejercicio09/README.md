Para este ejercicio partí del descriptor de ejemplo y lo modifiqué para que utilice la imagen de password-api y cree 3 replicas.

Luego ejecuté el comando 'kubectl apply -f deployment.yml'

A continuación, hice un get pods para ver las 3 replicas

kubectl get pods | grep passwordapi
passwordapi-5dd5f46c96-bvlfs   1/1     Running   0          4m55s
passwordapi-5dd5f46c96-ftls4   1/1     Running   0          4m55s
passwordapi-5dd5f46c96-khbsg   1/1     Running   0          4m55s

Me metí en el pod como sugería el enunciado del ejercicio
kubectl exec -it pod/passwordapi-5dd5f46c96-bvlfs -- bash

y ejecuté 'curl localhost:3000/password' para ver que estuviera andando.

Luego hice lo mismo para los 2 pods restantes.

