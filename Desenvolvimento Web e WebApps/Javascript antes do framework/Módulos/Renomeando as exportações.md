Neste vídeo, veremos como renomear exportações em JavaScript. Veremos a diferença entre exportações padrão e nomeadas, mostrando como renomear funções ao exportá-las com nomes diferentes.

Vamos voltar ao exemplo anterior.

```js
function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}

export { sum, multiply }
```

Agora vamos imaginar que você queira exportar a função com outro nome do que foi definido a elas.

```js
function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}

export { sum as sumTwoNumbers, multiply }
```

```js
import { sumTwoNumbers } from "./calc.js"

console.log(sumTwoNumbers(9, 8))
```
