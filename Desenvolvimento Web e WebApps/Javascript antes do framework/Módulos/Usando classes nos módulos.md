Neste vídeo, vamos aprender sobre o uso de classes em módulos. Vamos criar uma classe, exportá-la e adicionar métodos dentro dela.

É muito comum utilizarmos classes nos módulos, como visto anteriormente, as classes armazenam métodos e propriedades de alguma entidade da nossa aplicação.

```js
export class Calc {
	sum(a, b) {
		return a + b
	}
	
	multiply(a, b) {
		return a * b
	}
}
```

Dessa forma, precisamos corrigir a importação no `main.js`.

```js
import { Calc } from "./calc.js"

const calc = new Calc()

console.log(calc.sum(2, 4))
console.log(calc.multiply(2, 4))
```