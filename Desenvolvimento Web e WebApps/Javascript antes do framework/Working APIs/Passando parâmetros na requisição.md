Nesta aula, criaremos uma nova função em JavaScript para buscar um produto específico usando `async` e o `await`. Com a interpolação de strings, podemos passar o ID como parâmetro ao chamar a função. Assim, conseguimos buscar produtos específicos de forma dinâmica. É importante entender como passar parâmetros para requisições.

```js
async function fetchProductById(id) {
	const response = await fetch(`http://localhost:3333/products/${id}`)
	const data = response.json()

	console.log(data)
}

fetchProductById("3")
```

Dessa forma conseguirmos passar o `id` como parâmetro para a função, e usar esse `id` pra passar como parâmetro para requisição, buscando um produto pelo `id`.