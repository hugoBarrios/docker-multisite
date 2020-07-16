# Servidor multisitio con Docker Compose + SSL
Estructura de Docker Compose para levantar varios servidores web en la misma máquina haciendo uso de Apache como servidor web, PHP como lenguaje de scripting y Traefik como Proxy reverso y Let's Encrypt para generar certificados ssl.

## Requisitos
Tener Docker y Docker compose instalado

## Instrucciones
1) Modificar el email para emitir los certificados ssl que esta en el contenedor de traefik

2) Duplicar los contenedores de php-apache y crear uno por cada sitio web que se desea alojar y crear las carpetas para los volumenes en cada contenedor

3) Modificar los dominios que apuntan a cada uno de los contenedores

4) Crear registro de tipo A apuntando al servidor en todos los dominios del paso número 3

5) Ingresar al archivo docker-compose.yaml y configurar el límite de memoria ram que cada contenedor puede usar

6) Ir a la carpeta donde esta docker-compose.yaml y ejecutar ```docker-compose up -d```

7) ¡Disfruta!
