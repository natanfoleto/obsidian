
Nessa aula vamos aprender como sobrescrever métodos.

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
	makeNoise() {
		console.log("Au Au!")
	}	
}

const dog = new Dog("Pluto")
dog.makeNoise()

class Cat extends Animal {
	makeNoise() {
		console.log("Miau!")
	}
}

const cat = new Cat("Yummi")
cat.makeNoise()
```

Vamos adicionar métodos diferentes para as classes dog e cat. `run()`e `jump()`.