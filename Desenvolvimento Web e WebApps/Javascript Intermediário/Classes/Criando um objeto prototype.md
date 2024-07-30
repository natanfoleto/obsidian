Nesta aula, exploraremos a herança de objetos em JavaScript, demonstrando na prática o uso do prototype. Vamos aprender como objetos como endereço e arrays possuem protótipos que podem ser explorados para entender a cadeia de herança. Compreender essa estrutura de herança em JavaScript é fundamental para aprofundar seus conhecimentos na linguagem.

```js
const address = {
	city: "São paulo",
	country: "Brazil"
}
console.log(address)

const users = ["Natan", "João", "Maria"]
console.log(users)

const username = "Natan Foleto"
console.log(username.__proto__)
```
