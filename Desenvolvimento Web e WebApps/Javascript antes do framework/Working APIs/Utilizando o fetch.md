Nesta aula, veremos como consumir uma API utilizando JavaScript e a função `fetch`. Aprenderemos como definir o endereço da API, lidar com promises, obter informações da requisição e converter a resposta para JSON. Veremos a importância de lidar com requisições assíncronas e como utilizar o método `.then` para tratar os dados retornados pela API.

Agora dentro do `main.js` vamos utilizar o `fetch` para fazer as requisições. Ele é a API interna do `js` pra fazer requisições.

```js
const response = fetch("http://localhost:3333/products")

console.log(response)
```

Vamos iniciar o projeto com o `live-server` e visualizar o `console.log`. Logo podemos ver que o resultado é uma `Promise`. Como aprendemos anteriormente, toda função que depende de fatores externos, exemplo uma API, não retorna a resposta imediatamente.

Vamos utilizar primeiro a syntax do `.then, .catch e .finally` pra esperar essa `Promise` ser resolvida.

```js
fetch("http://localhost:3333/products")
	.then((response) => {
		console.log(response)
	})
```

Agora se visualizarmos o console, ele não é mais uma promessa, mas ainda não temos o retorno deseja. Esse retorno, são informações da requisição que fizemos.

Para pegarmos o resultado de fato, precisamos pegar o `response` e usar a função `.json()`. E como essa função `.json()` também é assíncrona, precisamos usar um `.then()` nela também.

```js
fetch("http://localhost:3333/products")
	.then((response) => {
		response.json()
			.then((data) => console.log(data))
	})
```