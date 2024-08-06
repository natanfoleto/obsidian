Nesta aula, veremos como utilizar o `async` e o `await` em vez do `then` para aguardar uma promise e obter dados de uma requisição. Veremos a diferença entre utilizar `async` e `await` e `then`, destacando que a escolha depende do cenário e preferência pessoal. O `async` e o `await` é útil em situações onde não é viável criar uma nova função.

Agora vamos utilizar o `async` e `await` para esperarmos a promessa da requisição.

```js
async function fetchProducts() {
	const response = await fetch("http://localhost:3333/products")
	const data = response.json()

	console.log(data)
}

fetchProducts()
```
