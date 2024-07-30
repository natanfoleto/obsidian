Nesta aula, aprenderemos a criar uma classe em JavaScript, utilizando a palavra reservada `class` seguida do nome da classe no padrão Paschal Case. Vamos entender um pouco a diferença entre Camel Case, Snake Case e Paschal Case. Iremos definir o corpo da classe e criar um construtor, que é uma função especial executada automaticamente ao instanciar a classe.

```js
class MyClass {
	
}

class Person {
	constructor() {
		console.log("Classe instanciada.")
	}
}

const person = new Person()
```

```js
	class Person {
	constructor(name) {
		console.log(`Olá ${name}`)
	}
}

const person = new Person("Natan")
```
