Nessa aula, veremos a diferença entre exportação `padrão` e `nomeada` em JavaScript. Veremos como exportar funções nomeadas e a função padrão, e como importá-las de forma separada. Destacaremos que a exportação `default` não requer chaves ao importar e que as funções nomeadas precisam ser importadas pelo nome exato.

```js
export function sum(a, b) {
	return a + b
}

export function multiply(a, b) {
	return a * b
}
```

Pegando o exemplo anterior, temos essa forma de exportação.
Agora veja o que acontece quando utilizamos a palavrinha `default` depois do `export`.

```js
// Essa é a exportação padrão
export default function sum(a, b) {
	return a + b
}

// Essa é a exportação nomeada
export function multiply(a, b) {
	return a * b
}
```

Ou seja, a função `sum` é a exportação padrão desse módulo, sendo assim eu só consigo ter ela como função disponível ao utilizar no arquivo `main.js`.

```js
// Isso não funciona mais.
import { sum } from "./calc.js"

// Apenas essa forma
import sum from "./calc.js"

console.log(sum(5, 9))
```

Se eu quiser utilizar as duas funções, eu posso além de fazer a importação padrão, utilizar a forma desestruturada junto.

```js
import sum, { multiply } from "./calc.js"

console.log(sum(5, 9))
console.log(multiply(3, 3))
```

O nome `sum` pouco importa, desde que eu esteja fazendo a exportação padrão. Diferente da nomeada, que utilizamos o próprio nome da função que estamos exportando.