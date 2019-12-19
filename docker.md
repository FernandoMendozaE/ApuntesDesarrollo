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
