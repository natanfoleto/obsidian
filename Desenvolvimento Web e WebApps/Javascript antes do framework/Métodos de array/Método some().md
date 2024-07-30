Nesta aula, vamos aprender o método `some()`, que verifica se pelo menos um elemento em um array atende a uma condição definida, retornando um valor booleano. Vamos utilizar um exemplo com um array de idades, onde o método `some()` foi aplicado para verificar se algum elemento é menor que 18. Se pelo menos um elemento atender à condição, o método retorna verdadeiro. Caso contrário, retorna falso.

```js
// O método some() testa se ao menos um dos elementos no array passa na condição e retorna um valor true ou false

const ages = [15, 30, 39, 29]

// Verifica se existe pelo menos um item for menor que 18
const result = ages.some((age) => age < 18)
console.log(result)
```