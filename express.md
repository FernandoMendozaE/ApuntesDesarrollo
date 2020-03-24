![EXPRESS logo](https://github.com/FernandoMendozaE/ApuntesDesarrollo/blob/master/image/express.PNG)

## Intalación

> ```
> npm install express
> ```

## Creación de un servicio básico en Express.

1. Configuración inicial

   > ```javascript
   > const express = require('express') //llamando al modulo express
   > const app = express() //obtiene el objeto express
   > ```

2. Configurando un puerto en express

   > ```javascript
   > app.listen(5000, () => {
   >   console.log('Serve on port 5000')
   > }) //levantar el servicio
   > ```

## Routing (enrutamiento)

- Tipos de peticiones HTTP:

  1. Petición **_GET_**

     > ```javascript
     > app.get('/user', (req, res) => {
     >   res.json({
     >     username: 'Cameron',
     >     lastname: 'Howe'
     >   }) //responde la petición
     > }) //recibe una peticion HTTP (get) y realiza algo
     > ```

  2. Petición **_POST_**

     > ```javascript
     > //:id : request parms (parametro recibido mediante la url)
     > app.post('/user/:id', (req, res) => {
     >   console.log(req.body) //obtiene datos del request json
     >   console.log(req.params) //obtiene datos del id (url) parametros
     >   res.send('POST REQUEST RECEIVED') //request post
     > })
     > ```
     >
     > **_Observacón_**: Generando rutas dinamicas (:id). Ejemplo de envió por url "localhost:5000/user/456"

  3. Petición **_PUT_**

     > ```javascript
     > //:id : request parms (parametro recibido mediante la url)
     > app.put('/user/:userId', (req, res) => {
     >   console.log(req.body)
     >   res.send(`User ${req.params.userId} update`)
     > })
     > ```
     >
     > **_Observacón_**: Generando rutas dinamicas (:id). Ejemplo de envió por url "localhost:5000/user/456"

  4. Petición **_DELETE_**

     > ```javascript
     > //:id : request parms (parametro recibido mediante la url)
     > app.delete('/user/:id', (req, res) => {
     >   res.send(`User ${req.params.id} deleted`) //responde la petición
     > })
     > ```
     >
     > **_Observacón_**: Generando rutas dinamicas (:id). Ejemplo de envió por url "localhost:5000/user/456"

- Función **_all_** de express

  La función _all_ se encarga de ejecutar todo contenido que tiene antes de ir a la ruta (get, post, etc)

  > ```javascript
  > // next encargado de que pase a la siguiente ruta (get, post, etc)
  > app.all('/user', (req, res, next) => {
  >   console.log('Por aqui paso')
  >   next()
  > }) // función express encargado de que pasen toda las rutas (/user)
  > ```

## Middlewares

Un middleware es una función que se puede ejecutar antes o después del manejo de una ruta.

- Ejemplo básico:

  > ```javascript
  > function logger(req, res, next) {
  >   console.log(
  >     `Router Received: ${req.protocol}://${req.get('host')}${
  >       req.originalUrl
  >     }` // muestra la ruta (host:   servidor)
  >   )
  >   next()
  > }
  >
  > // Middlewares
  > /**
  >  * Procesa datos antes de llegar a las rutas
  >  */
  > app.use(express.json()) // linea de código encargado de hacer conocer el formato JSON
  > app.use(logger)
  > ```

- Morgan: Es un middleware que nos permite registrar fácilmente solicitudes, errores y más en la consola.

  - **Intalación**
    > ```
    > npm i morgan
    > ```
  - **Uso:**
    > ```javascript
    > var morgan = require('morgan')
    > app.use(morgan('dev')) //muestra si llego la petición exitosamente
    > ```

  [Documentación de Morgan](https://www.npmjs.com/package/morgan)

  > ```
  >
  > ```
  >
  > ```
  >
  > ```
  >
  > ```
  >
  > ```

- _Configuración del archivo:_

  ![github](https://github.com/FernandoMendozaE/ApuntesDesarrollo/blob/master/image/ConfiguracionPM2.PNG)
