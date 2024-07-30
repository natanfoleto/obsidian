Nesta aula, focaremos no método `filter()`, que cria um novo array com elementos que atendem a uma condição. Demonstraremos como aplicar o `filter()` em um array de palavras e em um array de objetos.

```js
// O método filter() cria um novo array com todos os elementos que passaram na condição.

const words = ["Javascript", "HMTL", "CSS", "Web"]

const result = words.filter((word) => word.length > 3)

console.log(result)

const products = [
	{ description: "Teclado", price: 150, promotion: true },
	{ description: "Mouse", price: 70, promotion: false },
	{ description: "Monitor", price: 900, promotion: true }
]

const promotion = products.filter(() => product.promotion === true)

console.log(promotion)
```
