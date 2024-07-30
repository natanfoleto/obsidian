
```ts
function showTicket(user, ticket) {
	console.log(`Olá ${user}`. Seu número de bilhete é ${ticket})
}

showTicket('Natan Foleto', 123)
```

Vamos visualizar na aba .JS do TS playground, a saída do código compilado.



```ts
function showTicket(user, ticket) {
	console.log(`Olá ${user ?? 'Usuário padrão'}`. Seu número de bilhete é ${ticket})
}

showTicket('Natan Foleto', 123)
```

Agora vamos ver no código compilado o que ele adicionou após a mudança no código.