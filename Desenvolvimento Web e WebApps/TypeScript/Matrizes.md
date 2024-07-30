
No TypeScript, é possível definir tipagens para arrays, como de números ou strings. Ao declarar um array, é importante especificar o tipo dos elementos que ele irá conter. Caso haja uma tentativa de inserir um tipo diferente do especificado, o TypeScript irá gerar um erro. Existem duas maneiras de declarar um array: utilizando a sintaxe de colchetes ou a palavra-chave 'array'. Ambas formas são válidas, porém a preferência pessoal pode influenciar na escolha.

```ts
let numbers: number[]
numbers = [1,2,3,4,5,6, "Natan"]

let users: Array<string>
users = ['Natan', 'João']
```
