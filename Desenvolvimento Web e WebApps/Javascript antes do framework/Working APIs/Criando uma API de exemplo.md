Nesta aula, criaremos dados para simular uma API, definindo recursos como produtos. Utilizaremos o json-server para simular a API e testaremos acessando os produtos via navegador, fazendo requisições do tipo GET. Demonstraremos como filtrar produtos por ID e como simular o comportamento de uma API.

Agora vamos criar o conteúdo da nossa API. Cada chave criada no objeto do `json-server` é um recurso da API, mais pra frente vamos ver como realmente esses recursos/rotas são criados de fatos. O `json-server`, usa o objeto e cria uma API de acordo com o conteúdo do `json`, para simular uma API real.

```json
{
	"products": [
		{ "id": 1, "name": "Mouse", price: 150.25 },
		{ "id": 2, "name": "Teclado", price: 200 },
		{ "id": 3, "name": "Monitor", price: 900 },
		{ "id": 4, "name": "GTX 4090", price: 2900 },
	],
	"users": []
}
```

Cada chave ele entende como um `recurso/rota/endpoint`.

Agora podemos testar pelo navegador, fazendo uma requisição em `products` pra ver se o conteúdo da API está sendo retornado corretamente.

`localhost:3333/products`

O legal é que podemos passar parâmetros nas requisições, como filtros pra pegar um produto específico.

`localhost:3333/products/2`


É interessante notar que estamos utilizando o `browser` pra fazer as requisições, por padrão ele consegue fazer requisições do tipo `GET` pra buscar informações, mas a partir daqui iremos aprender utilizar o próprio `js` pra fazer essas requisições, e termos o resultado dessa API dentro do nosso código.