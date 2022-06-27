Primero creé el bot de telegram y obtuve el token.

Luego, lo probé corriendo localmente con el comando 'docker run -e TELEGRAM_TOKEN=<<PLACEHOLDER_FOR_TOKEN>> nicopaez/telegrambot:0.0.7' y le escribí para ver la versión.

Después de eso, hice stop del contenedor correspondiente, escribí el descriptor, ejecuté 'kubectl apply -f deployment.yml' y esperé a que levante un pod con la imagen correspondiente. Una vez que estuvo arriba volví a escribirle para que me diera la version.
