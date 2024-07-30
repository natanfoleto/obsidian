Nesta aula, aprenderemos sobre a desestruturação em JavaScript, uma técnica que facilita a extração de dados de arrays e objetos. Vamos aprender como desestruturar um array, pegando valores específicos e ignorando outros. A desestruturação é uma ferramenta poderosa para manipular dados de forma eficiente em JavaScript.

```js
// destructuring assignment (desestruturação) permite extrair dados de arrays ou objetos em variáveis distintas

const data = ["Natan Foleto", "rodrigo@email.com"]

// Desestruturando array
const [username, email] = data
console.log("Nome: ", username)
console.log("E-mail: ", email)

const fruits = ["Banana", "Apple", "Orange"]

// Desestruturando somente o primeiro
const [banana] = fruits
console.log(banana)

// Ignorando o primeiro na desestruturação
const [_, apple] = fruits
console.log(apple)

const [, , orange] = fruits
console.log(orange)
```
