O operador de `spread` permite expandir o conteúdo de um objeto iterável, como um array ou uma string, para ser usado em zero ou mais argumentos. É possível utilizar o `spread` para manipular e interagir com objetos de forma mais flexível. Com exemplos práticos, vamos demonstrar como o `spread` pode ser utilizado para expandir arrays e objetos, facilitando a manipulação e a interação com seus elementos de forma separada.

```js
// spread (espalhar) permite que um objeto iterável, como uma expressão de array ou uma string seja expandido para ser usado onde zero ou mais argumentos.

const numbers = [1, 2, 3]
console.log(numbers)

// Spread
console.log(...numbers)

// Criando array de objetos
const data = [
	{
		name: "Natan Foleto",
		email: "natan@email.com",
		avatar: "n.png"
	},
	{
		name: "João",
		email: "joao@email.com",
		avatar: "j.png"
	}
]

console.log(data)

// Usando spread no array com obj
console.log(...data)
```