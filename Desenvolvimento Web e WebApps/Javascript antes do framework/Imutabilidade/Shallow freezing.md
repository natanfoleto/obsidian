Nesta aula, vamos aprender como congelar um objeto em JavaScript para evitar modificações, utilizando o `object.freeze()`. Veremos que o `freeze()` não impede modificações profundas em objetos aninhados, realizando um congelamento raso. Após congelar o objeto, modificações em objetos aninhados ainda são possíveis.

```js
const book = {
	title: "Objetos Imutáveis",
	category: "javascript",
	author: {
		name: "Natan",
		email: "natan@email.com"
	}
}

// O javascript em si não impõe restrições à modificação dos objetos.
book.category = "HTML"

console.log(book)

Object.freeze(book)
book.category = "CSS" // não modifica mais

console.log(book)

// O Object.freeze não impede modificações profundas em objetos aninhados (shallow freezing)
book.author.name = "João"
console.log(book)
```