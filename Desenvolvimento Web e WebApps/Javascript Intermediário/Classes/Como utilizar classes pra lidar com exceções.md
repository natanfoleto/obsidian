Nesta aula, aprenderemos a utilizar classes para lidar com exceções específicas em JavaScript. Vamos ver como identificar e tratar diferentes tipos de erros, como TypeError e RangeError. Também foi abordado o uso do método `throwNew` para gerar exceções personalizadas. Vamos mostrar a importância de tratar exceções de forma específica e amigável para o usuário, assim como a possibilidade de encadear diferentes tipos de exceções.

```js
let obj = []

try {
	obj.execute()
} catch(error) {
	if (error instanceof TypeError) {
		console.log("Método indisponível.")
	}

	console.log(error)
}
```


```js
let obj = []

try {
	if (!obj.includes(17)) {
		throw new Error("O número 17 não está disponível")
	}
} catch(error) {
	if (error instanceof TypeError) {
		console.log("Método indisponível.")
	}

	console.log(error)
}
```
