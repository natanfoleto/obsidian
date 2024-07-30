Nesta aula, vamos aprender o método `reduce()`, utilizado para reduzir um array a um único valor, como por exemplo, somar todos os itens de uma lista. Os parâmetros do `reduce()` incluem o array original, o acumulador, o valor da iteração atual, o valor inicial e o índice (opcional).

```js
/*
	O método reduce é utilizado para reduzir um array a um único valor.

	Parâmetros:
	- Array original (values)
	- Acumulador (accumulator)
	- Valor da iteração (currentValue)
	- Valor inicial (0)
	- Index (index da iteração atual - opcional)
*/

const values = [1, 2, 3, 4, 5]

const sum = values.reduce((accumulator, currentValue, index) => {
	console.log("Acumulador: ", accumulator)
	console.log("Valor atual: ", currentValue)
	console.log("Index: ", index)

	console.log("Soma: ", accumulator + currentValue)
	console.log("#############")
	console.log(" ")
}, 0)

console.log("Resultado da soma final: ", sum)
```