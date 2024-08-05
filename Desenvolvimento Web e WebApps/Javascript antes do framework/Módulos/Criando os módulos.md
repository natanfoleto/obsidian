Nesta aula, foi criado o primeiro módulo em JavaScript. Foi mostrada a estrutura do projeto, com um arquivo index.html e um arquivo de scripts vazio renomeado para main.js. Foi criado um novo arquivo chamado calc.js para separar funcionalidades em módulos. Foram implementadas funções de soma e multiplicação nesse módulo, e explicado o uso de import e export para compartilhar funções entre módulos


Criando a estrutura,

```
index.html
script.js -> main.js
```

Agora vamos criar um novo módulo, pensando em um exemplo de um sistema que seria uma calculadora. Vamos criar um arquivo `calc.js`.

```js
function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}
```

Agora pra usar as funções, vamos chama-las no `main.js`.

```js
import { } from "./calc.js"
```

Não conseguimos importar nada ainda, porque no módulo de `calc`, precisamos falar pro JS, quais func iremos exportar.

```js
export function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}
```

A partir de agora a importação aparecerá.

```js
import { sum } from "./calc.js"

console.log(sum(4 + 6))
```

Ao executar esse código, receberemos um erro, dizendo que não podemos utilizar a sintaxe dos módulos. E ai precisamos adicionar essa configuração na tag `script` que está importando o JS em nosso HTML.

```html
<script type="module" src="main.js"></script>
```

Agora testamos novamente.

Podemos também exportar as funções usando essa notação:

```js
export { sum, multiply }
```