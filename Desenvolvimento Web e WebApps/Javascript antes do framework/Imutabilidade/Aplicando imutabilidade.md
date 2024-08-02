Nesta aula, abordaremos o conceito de imutabilidade na programação. Veremos como a manipulação de objetos pode gerar referências em vez de cópias, levando a alterações inesperadas.

```js
const address1 = {
	street: "Av. Brasil",
	number: 20
}

// Isso não é uma cópia. É uma referência.
const address2 = address1
address2.number = 30

console.log(address1, address2)
```

```js
// Aqui sim estamos criando um novo obj
const address2 = { ...address1 }
address2.number = 30

console.log(address1, addres2)
```

```js
// Precisa ser o spreed primeiro, pra não sobrepor o valor do original
const address2 = { ...address1, number: 30 }

console.log(address1, address2)
```

```js
const list1 = ["Apple", "Banana"]
const list2 = list1

list2.push("Watermelon")

console.log(list1, list2)
```

```js
const list2 = [...list1]
list2.push("Watermelon")

console.log(list1, list2)

// OU

const list2 = [...list, "Watermelon"]
console.log(list1, list2)
```