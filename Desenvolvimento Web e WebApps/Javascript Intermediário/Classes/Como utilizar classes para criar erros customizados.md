Nesta aula, aprenderemos a criar erros personalizados usando classes em JavaScript. A personalização de erros oferece flexibilidade na aplicação.

```js
class MyCustomError() {
	constructor(message) {
		this.message = "CLASSE DE ERRO CUSTOMIZADA: " + message
	}
}

try {
	throw new MyCustomError("Erro personalizado lançado!")
} catch(error) {
	if (error instanceof MyCustomError) {
		console.log(error)
	}
}
```

