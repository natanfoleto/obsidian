
No TypeScript, a tipagem explícita declara de forma clara o tipo das variáveis. Ao definir que uma variável é uma string ou um número, estamos explicitando o tipo. Isso permite que, ao chamar uma função, o TypeScript indique os tipos esperados. Ao preencher os parâmetros, a cor de destaque muda conforme o tipo esperado. A tipagem explícita é essencial para deixar claro o tipo de cada variável no código.

```ts
function showTicket(user, ticket) {
	console.log(`Olá ${user}`. Seu número de bilhete é ${ticket})
}

showTicket('Natan Foleto', 123)
```




