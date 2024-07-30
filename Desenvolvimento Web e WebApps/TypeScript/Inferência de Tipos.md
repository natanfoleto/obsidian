
Na programação, podemos declarar explicitamente o tipo de uma variável, como uma string. No TypeScript, também há a inferência de tipo, onde o TypeScript reconhece automaticamente o tipo da variável com base no conteúdo atribuído a ela. Isso permite que não seja necessário declarar explicitamente o tipo em todas as variáveis. Se tentarmos atribuir um valor de tipo diferente ao que foi inferido, como um número em vez de uma string, ocorrerá um erro. A inferência de tipo facilita a programação no TypeScript.

```ts
let user: string = "Natan Foleto"
let user = "Natan Foleto"

user = 10
```

