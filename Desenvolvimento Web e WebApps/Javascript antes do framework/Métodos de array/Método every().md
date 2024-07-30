Nessa aula vamos aprender sobre o método `every()` que verifica se todos os elementos de um array atendem a uma condição, retornando um valor booleano. Por exemplo, ao verificar se todas as idades em um array são maiores ou iguais a 18, o resultado será `false` se houver pelo menos um valor abaixo de 18. O uso do `console.log` ajuda a visualizar o resultado.

```js
// O método every() testa se todos os elementos do array passam na condição e retorna um valor Boolean.

const ages = [15, 30, 39, 29]

// Verificando se todas as idades são maiores ou igual a 18
const result = ages.every((age) => age >= 18)
console.log(result)
```