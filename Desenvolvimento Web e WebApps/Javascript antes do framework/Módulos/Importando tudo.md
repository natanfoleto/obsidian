Nesta aula veremos como importar tudo de uma vez.

```js
function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}

export { sum, multiply }
```

Para importar tudo de uma vez, na importação escrevemos dessa forma:

```js
// Um por vez
import { sum, multiply } from "./calc.js"

// Tudo de uma vez
import * as calc from "./calc.js"

// Pra usar agora com essa importação

console.log(calc.sum(3, 2))
```