
Nesta aula, veremos como fazer a intersecção entre tipos no contexto de programação.

```ts
type User = {
	id: number
	name: string
}

type Char = {
	nickname: string
	level: number
}

type PlayerInfo = User & Char

let info: PlayerInfo = {
	id: 1,
	name: "João Vitor",
	nickname: "birobirobiro",
	level: 50,
}
```
