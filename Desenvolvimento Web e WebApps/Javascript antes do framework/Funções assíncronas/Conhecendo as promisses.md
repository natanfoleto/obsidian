Nesta aula, veremos como criar e utilizar uma promise em JavaScript. Aprenderemos sobre o uso de `resolve`, `reject`, `then`, `catch` e `finally` para lidar com o sucesso e falha da promises. O uso correto desses métodos permite controlar o fluxo de execução de operações assíncronas.

```js
// Função que retorna uma Promise.

function asyncFunction() {
	return new Promise((resolve, reject) => {
		// Simula uma operação assíncrona
		const isSuccess = true

		if (isSucess) {
			resolve("A operação foi concluída com sucesso!")
		} else {
			reject("Algo deu errado!")
		}
	})
}
```

Essa função recebe o retorno de uma chamada de outra função, que seta o valor de `ìsSucess` como `true` ou `falso`. Ai dependendo do retorno, ela da um `resolve` ou `reject`.

Agora vamos simular essa chamada, onde ela levaria um tempo pra ser executada.

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

// Visualizando que o retorno é uma promise
console.log(asyncFunction())

// Como pedir pro javascript esperar ela ser executada, pra visualizar o retorno
console.log("Executando função assíncrona...")

asyncFunction()
	.then((response) => {
		console.log("Sucesso: ", response)
	})
	.catch((error) => {
		console.log("Error: ", error)
	})
	.finally(() => {
		console.log("Fim da execução")
	})
```