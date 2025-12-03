# Imagen base: NGINX
FROM nginx:alpine

# Copiamos el HTML al directorio por defecto de NGINX
COPY ./app/index.html /usr/share/nginx/html/index.html

# Exponemos el puerto 80 (interno del contenedor)
EXPOSE 80