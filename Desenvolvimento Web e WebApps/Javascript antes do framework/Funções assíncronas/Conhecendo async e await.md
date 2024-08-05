Neste vídeo, veremos como utilizar `async` e `await` para lidar com funções assíncronas. Vamos aprender como utilizar `async` antes da função para lidar com `await`, aguardando a resolução ou rejeição da promise. Também vamos aprrender como lidar com exceções utilizando try, catch e finally.

```js
function asyncFunction() {
	return new Promise((resolve, reject) => {
		// Simula uma operação assíncrona
		setTimeout(() => {
			const isSuccess = true

			if (isSucess) {
				resolve("A operação foi concluída com sucesso!")
			} else {
				reject("Algo deu errado!")
			}
		}, 3000) // Simula uma operação que leva 3 segundos
	})
}
```

Uma das maneiras de executar funções assíncronas é utilizando as `Promises` como vimos anteriormente. Mas existe outra forma também de fazer isso, usando o `async` e `await`. Vamos ao exemplo abaixo:

```js
function fetch() {
	const response = asyncFunction()
	console.log(response)
}

fetch()
```

Dessa forma podemos ver que o `response` é uma `Promise` pendente.

```js
async function fetch() {
	const response = await asyncFunction()
	console.log(response)
}

fetch()
```

Caso estiver usando a notação de `arrow functions`.

```js
const fetch = async () => {
	const response = await asyncFunction()
	console.log(response)
}

fetch()
```

Talvez neste momento, venha uma dúvida... E o bloco que tratava a exceção (`catch`) e (`finally`) na primeira utilização das `promises`?

Bom, basta utilizarmos o bloco de `try`, `catch`, `finally` que teremos o mesmo resultado.

```js
async function fetch() {
	try {
		const response = await asyncFunction()
		console.log("Sucesso: ", response)
	} catch(error) {
		console.log("Error: ", error)
	} finally {
		console.log("Execução finalizada!")
	}
}

fetch()
```


Vantagens do `async/await`.

* Sintaxe Mais Clara e Legível
* Tratamento de Erros Mais Simples
* Fluxo de Controle Sequencial
* Debugging Mais Fácil