Nesta aula, abordaremos o método `find()` em JavaScript, que retorna o primeiro elemento de um array que satisfaz uma condição.

```js
// O método find() retorna o valor do primeiro elemento do array que satisfazer a condição. Caso contrario, undefined é retornado.

const values = [5, 12, 8, 130, 44]

// Retorna o primeiro elemento que o valor é maior que 10
const found = values.find((value) => value > 10)
console.log(found)

// Exemplo com objetos
const fruits = [
	{ name: "apples", quantity: 23 },
	{ name: "bananas", quantity: 25 },
	{ name: "oranges", quantity: 52 }
]

const result = fruits.find((fruit) => fruit.name === "bananas")
const result = fruits.find((fruit) => fruit.quantity > 10)
```