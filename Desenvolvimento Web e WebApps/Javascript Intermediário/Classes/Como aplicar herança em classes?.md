Nesta aula, vamos aprender como aplicar herança com classes em programação. A herança permite reutilizar propriedades e métodos de classes superiores.

```js
class Animal {
	constructor(name) {
		this.name = name
	}

	makeNoise() {
		console.log("Algum som genérico do animal")
	}
}

class Dog extends Animal {
	// Não tem nada aqui	
}

const dog = new Dog("Pluto")
dog.makeNoise()
```

```js
class Cat extends Animal {
	// Não tem nada aqui
}

const cat = new Cat("Yummi")
cat.name
```