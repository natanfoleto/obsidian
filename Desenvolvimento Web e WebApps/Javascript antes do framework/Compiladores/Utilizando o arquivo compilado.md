Nesta aula, veremos como compilar um arquivo JavaScript utilizando o Babel para gerar a pasta dist. Aprenderemos a importância de compilar o código sempre que houver alterações, garantindo a compatibilidade com navegadores mais antigos.

Vamos adicionar mais funcionalidades na nossa classe.

```js
class User {
	constructor({ email }) {
		this.email = email
	}

	sendMessage() {
		console.log("Mensagem enviada para:", this.email)
	}
}

let user = new User({ email: "natanfoleto@email.com" })
user.sendMessage()
```

Agora vamos executar novamente o `build`, pra atualizar o código compilado com as novas alterações que fizemos.

Nesse momento, vamos rodar o nosso projeto usando o código compilado, pra testar se ele esta funcionando corretamente.

Dentro do `HTML`, vamos apontar o script para o `main.js` da pasta `dist`. E testaremos...
Basta visualizar o console do navegador pra ver se o teste deu certo.