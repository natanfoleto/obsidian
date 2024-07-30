Nesta aula, exploraremos o método `map()` para percorrer e manipular arrays. Com o `map()`, podemos passar uma função de callback para executar em cada elemento do array original, criando um novo array com base nos retornos. Demonstraremos como percorrer e formatar os itens do array, além de criar um novo array com objetos personalizados. O método `map()` é útil para manipular arrays e retornar um novo array ao final do processo.

```js
// O método map() chama a função callback recebida por parâmetro para cada elemento do Array original, em ordem, e constrói um novo array com base nos retornos de cada chamada. E no final devolve o novo array.

const products = ["Teclado", "Mouse", "Monitor"]

// Percorrendo os itens do Array
products.map((product) => {
	console.log(product)
})

// Sintaxe reduzida
products.map((product) => console.log(product))

// Utilizando o novo array retornado
const formatted = products.map((product => {
	return product.toUpperCase()

	return {
		id: Math.random(),
		description: product
	}
}))

console.log(formatted)
```