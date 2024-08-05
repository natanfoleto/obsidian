Nesta aula, veremos o uso do `setInterval` em comparação com o `setTimeout`. O `setInterval` executa uma função repetidamente em intervalos definidos, ao contrário do `setTimeout` que executa a função após um determinado tempo. Essa técnica é útil para controlar a execução de funções em intervalos específicos.

```js
// setInterval() exevuta uma função após um intervalo de tempo especificado.

let value = 10

setInterval(() => {
	console.log(value)
	value--
}, 1000)
```

Dessa forma o nosso intervalo irá executar infinitamente. Pra isso precisamos de uma forma de para-lo.

```js
const interval = setInterval(() => {
	console.log(value)
	value--
	
	if (value === 0) {
		console.log("Feliz ano novo!!!")

		// Interrompe o intervalo de execuções
		clearInterval(interval)
	}
}, 1000)
```

Agora a `const` interval vai armazenar a ref na memória, então quando o value for = 0 eu vou usar a função `clearInterval(interval)` passando o próprio intervalo como parâmetro.