
Interfaces são uma forma de declarar e criar tipos no TypeScript. Elas permitem definir a estrutura de um objeto, indicando quais propriedades são obrigatórias e quais são opcionais. Ao utilizar interfaces, podemos garantir a consistência e a tipagem dos dados em nosso código. Além disso, as interfaces podem ser utilizadas não apenas para objetos, mas também para definir tipos de parâmetros em funções. Dessa forma, facilitam a organização e a manutenção do código.

```ts
interface User {
	id: number
	name: string
}

let newUser: User = {
	id: 1,
	name: "Charles",
}

function registerNewUser(newUser: User) {
	newUser.id
	newUser.name
}
```

