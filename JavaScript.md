### JavaScript

```javascript
// function declaration
function saludar(nombreCliente) {
  console.log('Bienvenido ' + nombreCliente)
}

saludar('Juan')
```

> Enviando variables a una función

```javascript
//function expression
const cliente = function(nombreCliente) {
  console.log('Mostrando datos del cliente: ', nombreCliente)
}

cliente('Juan')

// Parametros por default en las funciones
function actividad(nombre = 'Walter White', actividad = 'Enseñar Quimica') {
  console.log(`La persona ${nombre}, esta realizando la actividad ${actividad}`)
}
actividad('Juan', 'Aprender JavaScript')
actividad('Pedro', 'Aprender JavaScript')
actividad('Antonio')
```

- **Arrow functions:** Las funciones de flecha se introdujeron con ES6 como una nueva sintaxis para escribir funciones de JavaScript. Ahorran tiempo a los desarrolladores y simplifican el alcance de la función.

```javascript
// arrow functions
let viajando = function(destino) {
  return `Viajando a la ciudad de: ${destino}`
}
let viaje
viaje = viajando('Paris')
viaje = viajando('Londres')
viaje = viajando('Barcelona')
console.log(viaje)

// arrow functions simplified
let viajando2 = destino => `Viajando a la ciudad de: ${destino}`
let viaje2
viaje2 = viajando2('Paris')
console.log(viaje2)
```
