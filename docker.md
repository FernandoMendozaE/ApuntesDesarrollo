# Docker

## Paso 1

Crear el archivo **_Dockerfile_** en la raiz del proyecto actual.

Configuracion del archivo _Dockerfile_:

> ```
> FROM node:12            // especifica el tipo de versión de node para que corra el proyecto
> WORKDIR /app            // especifica donde ira el proyecto (directorio de trabajo)
> COPY package*.json ./   // copia los archivos del proyecto al directorio de trabajo
> RUN npm install         // ejecuta comandos (se crea el node_module)
> COPY . .                // copia toda la carpeta del proyecto actual
> CMD ["npm", "start"]    // ejecutar el proyecto
> ```

- **Ignorar carpetas en docker**

  Crear el archivo _**.dockerignore**_ en la raiz del proyecto actual.

  Configuracion del archivo _dockerignore_:

  > ```
  > node_module
  > npm-debug.log
  > ```

## Paso 2

Creación de una **_imagen_**
En la terminal:

creación de una imagen

> ~/Desktop/Docker/**docker build -t _nombre_imagen_ .**

ver las imagenes creadas

> ~/Desktop/Docker/**docker images**

ejecuctar la imagen (-it: muestra por consola como se esta ejecutando, -p: cambia puerto "4000" de la ejecución del proyecto)

> ~/Desktop/Docker/**docker run -it -p 4000:3000 _nombre_imagen_**

ejecutando imagen en un proceso

> ~/Desktop/Docker/**docker run -d -p 4000:3000 _nombre_imagen_**

comprobar que procesos se estan ejecutando

> ~/Desktop/Docker/**docker ps**

parar un proceso que se estan ejecutando

> ~/Desktop/Docker/**docker stop _id_docker_**

ver todo los procesos que se estaban ejecutando

> ~/Desktop/Docker/**docker -a**
