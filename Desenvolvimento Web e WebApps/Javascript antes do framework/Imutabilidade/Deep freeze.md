Nesta aula, vamos ver como implementar o conceito de Deep Freeze em JavaScript, que consiste em congelar de forma profunda um objeto, percorrendo recursivamente cada propriedade. Vamos aprender como criar uma função recursiva para congelar todas as propriedades de um objeto, garantindo um congelamento profundo.

```js
const book = {
	title: "Objetos Imutáveis",
	category: "javascript",
	author: {
		name: "Natan",
		email: "natan@email.com"
	}
}

console.log(book)

Object.freeze(book)
book.category = "CSS"

book.author.name = "João"
console.log(book)

console.log(book)
```

```js
function deepFreeze(object) {
	// Obtém um array com todas as propriedades do objeto.
	const props = Reflect.ownKeys(object)

	console.log(props) // só pra ver as props

	// Itera sobre todas as propriedades do objeto
	for (const prop of props) {
		// Obtém o valor associado à propriedade atual
		const value = object[prop]
		console.log(value) // só pra ver os values

		// Verifica se o valor é um objeto ou uma função
		if (value && typeof value === "object" || typeof value === "function") {
			deepFreeze(value)
		}
	}

	// Retorna o objecto congelado
	return Object.freeze(object)
}

// Chama a função pra congelar o objeto com oo Deep Freeze (congelamento profundo)
deepFreeze(book)

book.category = "HTML" // Tentando mudar no primeiro nível
book.author.name = "João" // Tentando mudar no próximo nível

console.log(book)
```