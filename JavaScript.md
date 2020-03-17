![Javascript logo](https://www.manuprieto.es/wp-content/uploads/2017/07/javascript-icon.png)

# JavaScript

## Funciones

Una función es un procedimiento en JavaScript un conjunto de sentencias que realizan una tarea o calculan un valor. Para usar una función, debe definirla en algún lugar del ámbito desde el cual desea llamarla.

> ```javascript
> // function declaration
> function saludar(nombreCliente) {
>   console.log("Bienvenido " + nombreCliente);
> }
>
> saludar("Juan");
> ```

- **Funciones con parametros**

> ```javascript
> //function expression
> const cliente = function(nombreCliente) {
>   console.log("Mostrando datos del cliente: ", nombreCliente);
> };
>
> cliente("Juan");
>
> // Parametros por default en las funciones
> function actividad(nombre = "Walter White", actividad = "Enseñar Quimica") {
>   console.log(
>     `La persona ${nombre}, esta realizando la actividad ${actividad}`
>   );
> }
> actividad("Juan", "Aprender JavaScript");
> actividad("Pedro", "Aprender JavaScript");
> actividad("Antonio");
> ```

- **Arrow functions:** Las funciones de flecha se introdujeron con ES6 como una nueva sintaxis para escribir funciones de JavaScript. Ahorran tiempo a los desarrolladores y simplifican el alcance de la función.

> ```javascript
> // arrow functions
> let viajando = function(destino) {
>   return `Viajando a la ciudad de: ${destino}`;
> };
> let viaje;
> viaje = viajando("Paris");
> viaje = viajando("Londres");
> viaje = viajando("Barcelona");
> console.log(viaje);
>
> // arrow functions simplified
> let viajando2 = destino => `Viajando a la ciudad de: ${destino}`;
> let viaje2;
> viaje2 = viajando2("Paris");
> console.log(viaje2);
> ```

## Objetos

Un objeto es una colección de propiedades, y una propiedad es una asociación entre un nombre (o clave) y un valor.

- **Objetos y propiedades**

  Las propiedades de un objeto definen las características de un objeto;se puede acceder a ellas con una simple notación de puntos:

  > ```javascript
  > nombreObjeto.nombrePropiedad;
  > ```

  **_Ejemplo:_** Vamos a crear un objeto llamado **miAuto** y le vamos a asignar propiedades denominadas marca, modelo, y año de la siguiente manera:

  > ```javascript
  > var miAuto = new Object(); // intanciando objecto
  > miAuto.marca = "Ford";
  > miAuto.modelo = "Mustang";
  > miAuto.año = 1969;
  > ```

  Las propiedades no asignadas de un objeto son undefined (y no null).

  > ```javascript
  > miAuto.color; // undefined
  > ```

  Las propiedades de los objetos en JavaScript también pueden ser accedidas o establecidas mediante la notación de corchetes. _Los objetos son llamados a veces arreglos asociativos, ya que cada propiedad está asociada con un valor de cadena que puede ser utilizada para acceder a ella._

  **_Ejemplo:_** Puedes acceder a las propiedades del objeto **miAuto** de la siguiente manera:

  > ```javascript
  > miAuto["marca"] = "Ford";
  > miAuto["modelo"] = "Mustang";
  > miAuto["año"] = 1969;
  > ```

  El nombre de alguna propiedad que tenga un espacio o un guión, o comienza con un número sólo puede ser accedido utilizando la notación de corchetes. Esta notación es muy útil también cuando los nombres de propiedades son determinados dinámicamente (cuando el nombre de la propiedad no se determina hasta su tiempo de ejecución).

  **_Ejemplo:_** Esto se muestran a continuación:

  > ```javascript
  > var miObjeto = new Object(),
  >   cadena = "miCadena",
  >   aleatorio = Math.random(),
  >   objeto = new Object();
  >
  > miObjeto.type = "Sintaxis con punto";
  > miObjeto["Fecha de creación"] = "Cadena con espacios y acento";
  > miObjeto[cadena] = "String value";
  > miObjeto[aleatorio] = "Número Aleatorio";
  > miObjeto[objeto] = "Objeto";
  > miObjeto[""] = "Incluso una cadena vacía";
  >
  > console.log(miObjeto);
  > ```

  **_Recorrer un objeto_**

* **Listar las propiedades de un objeto**

  - **Bucles _for...in_**

    Este método recorre todas las propiedades enumerables de un objeto y su cadena de prototipo.
    Se puede utilizar la notación de corchetes con **for ... in** para iterar sobre todas las propiedades enumerables de un objeto.

    **_Ejemplos:_** Esto se muestran a continuación:

    > ```javascript
    > const object = { a: 1, b: 2, c: 3 };
    >
    > for (const property in object) {
    >   console.log(`${property}: ${object[property]}`);
    > }
    >
    > // expected output:
    > // "a: 1"
    > // "b: 2"
    > // "c: 3"
    >
    > // EJEMPLO  2
    > var miAuto = new Object();
    > miAuto.marca = "Ford";
    > miAuto.modelo = "Mustang";
    > miAuto.año = 1969;
    >
    > function mostrarPropiedades(objeto, nombreObjeto) {
    >   var resultado = ``;
    >   for (var i in objeto) {
    >     //objeto.hasOwnProperty se usa para filtrar (si exite) las propiedades  del objeto, return (true o false)
    >     if (objeto.hasOwnProperty(i)) {
    >       resultado += `${nombreObjeto}.${i} = ${objeto[i]}\n`;
    >     }
    >   }
    >   return resultado;
    > }
    > console.log(mostrarPropiedades(miAuto, "miAuto"));
    >
    > // Retorna:
    > // miAuto.marca = Ford
    > // miAuto.modelo = Mustang
    > // miAuto.annio = 1969
    > ```

    > Ejemplo de uso _hasOwnPropertydevuelve_
    >
    > ```javascript
    > var x = {
    >   y: 10
    > };
    > console.log(x.hasOwnProperty("y")); //true
    > console.log(x.hasOwnProperty("z")); //false
    > ```

  - **Object.keys(o)**

    Este método devuelve una matriz con todos los nombres de propiedades ("keys") enumerables y propias (no de la cadena de prototipos) de un objeto o.

    **_Ejemplo:_** Esto se muestran a continuación:

    > ```javascript
    > const object1 = {
    >   a: "somestring",
    >   b: 42,
    >   c: false
    > };
    >
    > console.log(Object.keys(object1));
    > // expected output: Array ["a", "b", "c"]
    > ```

    > ```
    >
    > ```

> #### Created by Fernando Mendoza Escobar with :blue_heart: :yellow_heart: :earth_americas:
>
> [Fernando](https://www.facebook.com/fernando.mendozaescobar)
>
> [My Github](https://github.com/FernandoMendozaE)
