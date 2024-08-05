Nesta aula, aprenderemos a renomear a importação de funções em JavaScript. É importante renomear as importações para evitar conflitos de nomes com funções já existentes. Podemos renomear as importações para letras ou palavras diferentes, tornando o código mais claro e organizado. Renomear a importação é útil quando importamos módulos com nomes semelhantes aos que já estamos utilizando. Essa prática ajuda a evitar conflitos e a manter o código mais legível.

Continuando com exemplo anterior.

```js
function sum(a, b) {
	return a + b
}

function multiply(a, b) {
	return a * b
}

export { sum, multiply }
```

```js
import { sum as sumTwoNumbers, multiply as m } from "./calc.js"

console.log(sumTwoNumbers(9, 8))
console.log(m(9, 8))
```

Isso é muito útil quando vamos importar algo que tem o mesmo nome que alguma função ou variável já criada no mesmo arquivo.