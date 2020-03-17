![PM2 logo](https://github.com/FernandoMendozaE/ApuntesDesarrollo/blob/master/image/pm2.png)

## Intalación

> ```
> npm install -g pm2
> ```

Ver versión de PM2:

> ```
> pm2 --version
> ```

## Comandos PM2

Ejecuta un procesos en PM2

> ```
> pm2 start project-1/index.js
> ```

Listar los servicios que se estan ejecutando

> ```
> pm2 list
> ```

Reiniciar los nuevos cambios de la apliación

- _Reiniciar proceso por ruta archivo_
  > ```
  > pm2 restart project-1/index.js
  > ```
- _Reiniciar proceso por id_

  > ```
  > // 0 indica el número del id
  > pm2 restart 0
  > ```

Parar la ejecución del la apliación

- _Parar proceso por ruta archivo_
  > ```
  > pm2 stop project-1/index.js
  > ```
- _Parar proceso por id_

  > ```
  > // 0 indica el número del id
  > pm2 stop 0
  > ```

Comando **all**

- _Parar todo los procesos_

  > ```
  > pm2 stop all
  > ```

- _Levantar todo los procesos_

  > ```
  > pm2 start all
  > ```

- _Eliminar todo los procesos_

  > ```
  > pm2 delete all
  > ```

Comando **--watch**

- _Comando encargado de reiniciar automáticamente su aplicación cuando se modifica un archivo en el directorio actual o sus subdirectorios_

  > ```
  > pm2 start project-1/index.js --watch
  > ```

Comando **--name**

- _Asigna un nombre al proceso_

  > ```
  > pm2 start project-2/index.js --name project-2
  > ```

Comando **log**

- _Muestra el historial de los procesos_

  > ```
  > pm2 log
  > ```

Comando **startup** (solo en linux)

- _Reinicia los procesos automaticamente al reiniciar_

  > ```
  > pm2 startup
  > ```

- _Cancelar los procesos automaticamente_

  > ```
  > pm2 unstartup
  > ```

Comando **startup**

- _Crea un archivo de configuración_

  > ```
  > pm2 ecosystem
  > ```

- _Configuración del archivo:_

  ![github](https://github.com/FernandoMendozaE/ApuntesDesarrollo/blob/master/image/ConfiguracionPM2.PNG)

> #### Created by Fernando Mendoza Escobar with :blue_heart: :yellow_heart: :earth_americas:
>
> [Fernando](https://www.facebook.com/fernando.mendozaescobar)
>
> [My Github](https://github.com/FernandoMendozaE)
