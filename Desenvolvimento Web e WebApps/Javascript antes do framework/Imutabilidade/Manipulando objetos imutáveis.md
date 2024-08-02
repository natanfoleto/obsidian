Nesta aula, aprenderemos a manipular objetos utilizando o princípio da imutabilidade. Em vez de modificar o objeto original diretamente, criamos um novo objeto com as alterações desejadas. Utilizamos o `spread` para preservar as propriedades existentes e modificar apenas as desejadas. Também veremos como adicionar novas propriedades e remover propriedades existentes usando o operador de desestruturação. Assim, conseguimos manipular objetos sem modificar o original, mantendo-o intacto.

```js
const book = {
	title: "Objetos Imutáveis",
	category: "javascript",
	author: {
		name: "Natan",
		email: "natan@email.com"
	}
}

const updatedBook = {
	...book,
	title: "Criando um front-end moderno com HTML",
	category: "html"
	// Podemos até adiconar mais props se quiser
}

// Original
console.log(book)

// Modificado
console.log(updatedBook)

// Utilizando operador de desestruturação (rest operator) para remover propriedades.

const { category, ...bookWithoutCategory } = book

console.log(bookWithoutCategory)
```
