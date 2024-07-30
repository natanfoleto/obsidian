Nesta aula, vamos aprender o conceito de método estático em programação. Vamos ver como criar e utilizar um método estático em uma classe, destacando a diferença de acesso entre métodos estáticos e não estáticos. Demonstraremos que métodos estáticos podem ser acessados sem a necessidade de instanciar a classe, enquanto métodos não estáticos requerem a instanciação da classe.

```js
class User {
	showMessage() {
		console.log("Essa é uma mensagem!")
	}
}

const user = new User()
user.showMessage()
```

```js
class User {
	static showMessage() {
		console.log("Essa é uma mensagem!")
	}
}

// const user = new User()
// user.showMessage()

User.showMessage()
```

```js
class User {
	constructor(message) {
		this.message = message
	}
	
	static showMessage(message) {
		console.log(message)
	}
}

// const user = new User()
// user.showMessage()

User.showMessage("Essa é uma mensagem!")
```