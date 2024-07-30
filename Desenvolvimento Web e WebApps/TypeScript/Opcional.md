
Propriedades de objetos podem ser opcionais, não obrigatórias. É possível definir propriedades que não precisam ser preenchidas ao criar um objeto. Para isso, basta adicionar um ponto de interrogação após o nome da propriedade, tornando-a opcional. Dessa forma, não será necessário informar essa propriedade sempre que um novo objeto for criado. Isso é útil quando se deseja definir propriedades que são necessárias apenas em casos específicos, como administradores, por exemplo.

```ts
type User = {
	name: string
	email: string
	age: number
	isAdmin?: boolean // isAdmin não será obrigatória na sua declaração
}

let newUser: User = {
	name: "João",
	email: "joao@email.com",
	age: 18,
}
```

