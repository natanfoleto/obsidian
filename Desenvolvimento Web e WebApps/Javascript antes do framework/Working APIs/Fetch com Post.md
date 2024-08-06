Nesta aula, aprenderemos a utilizar o método POST para enviar dados e cadastrar um novo produto na API. Criaremos um formulário no HTML para coletar informações do usuário e utilizaremos JavaScript para enviar esses dados para a API. Demonstraremos como configurar a requisição `fetch` com o método POST, definir o tipo de conteúdo como JSON e serializar os dados antes do envio. Ao final, testaremos o cadastro de produtos na API.

Até aqui utilizamos o método `GET` para fazer requisições, ele é usado pra buscar dados, mas se quisermos fazer requisições pra enviar dados pra API, e cadastrar novos produtos, conseguimos utilizando o método `POST`.

Para capturar os dados do novo produto que vamos cadastrar, vamos ao `HTML` e criar um `form` para fazer isso.

```html
<form>
	<input id="name" placeholder="Nome do produto">
	<input id="price" placeholder="Preço do produto">

	<button type="submit">Cadastrar</button>
</form>
```

Agora vamos para o `js` e criar a função que irá cadastrar um novo produto.

```js
// Pega o form pra usarmos o onsubmit
const form = document.getElementByTagName("form")

// Pega o nome e o preço do produto
const productName = document.getElementById("name")
const productPrice = document.getElementById("price")

addEventListener("submit", (event) => {
	event.preventDefault()

	fetch("http://localhost:3333/products", {
		method: "POST",
		headers: {
			"Content-Type": "application/json"
		},
		body: JSON.stringify({
			id: new Date().getTime().toString(),
			name: productName.value,
			price: productPrice.value,
		})
	})

	// Após cadastrar quero, exibir uma mensagem de sucesso
	// Mas precisamos adicionar o await antes do fetch que cadastra o produto
	// Senão ele não vai esperar o cadastro, e mostrar o alerta antes que o novo seja cadastrado
	alert("Novo produto cadastrado com sucesso!")
})
```

Para visualizarmos se o produto foi realmente cadastrado, podemos abrir o arquivo `server.json` e ver se o novo produto foi adicionado lá.