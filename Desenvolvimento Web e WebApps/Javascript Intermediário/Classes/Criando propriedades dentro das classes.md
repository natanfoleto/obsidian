Nesta aula, vamos aprender um pouco mais sobre o uso do `this` em classes em JavaScript, mostrando como criar propriedades e acessá-las.

```js
class Product {
	constructor(name) {
		this.name = name
	}
}

const product = new Product("Teclado")

console.log(product.name)
```

```js
const product1 = new Product("Mouse")

console.log(product1.name)
```
