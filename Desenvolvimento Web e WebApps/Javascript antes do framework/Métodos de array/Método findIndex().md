Nessa aula iremos estudar o método `findIndex()` que é responsável por retornar o índice do primeiro elemento que satisfaz uma condição em um array. Se nenhum elemento satisfizer a condição, ele retorna "-1". É importante lembrar que o índice retornado começa em 0. O método utiliza uma função de callback para percorrer o array e verificar a condição definida. Caso nenhum elemento satisfaça a condição, ele retorna "-1". O `findIndex()` é útil para encontrar a posição do primeiro elemento que atende a uma condição específica no array.

```js
// O método findIndex() retorna o índice no array do primeiro elemento que satisfazer a condição. Caso contrário, retorna -1, indicando que nenhum elemento passou no teste.

const values = [1, 50, 23, 48]

// Obtendo o primeiro indece que o valor é maior que 25
const index = values.findIndex((value) => value > 25))

console.log(index)
console.log(values[index])
```
