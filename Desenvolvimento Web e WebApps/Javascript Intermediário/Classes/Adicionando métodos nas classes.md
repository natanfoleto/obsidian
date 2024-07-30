  
Nesta aula, vamos aprender como adicionar métodos em classes em JavaScript. Veremos que não é necessário usar a palavra-chave `function` ao definir um método dentro de uma classe.

```js
class User {
	constructor(name, email) {
		this.name = name
		this.email = email
	}

	sendEmail() {
		console.log(`E-mail enviado para ${this.name} no endereço ${this.email}`)
	}
}

const user = new User("Natan", "natan@email.com")

user.sendEmail()
```
