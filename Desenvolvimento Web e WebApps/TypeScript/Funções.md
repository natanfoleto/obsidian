
Vamos abordar agora, como fazer a tipagem de funções em TypeScript. Uma função pode ter ou não um retorno, sendo void quando não há retorno. O TypeScript pode inferir automaticamente o tipo de retorno com base no conteúdo retornado. Vamos declarar explicitamente o tipo de retorno de uma função, utilizando dois pontos seguidos do tipo desejado. E vamos omitir a declaração do tipo de retorno e deixar o TypeScript inferir automaticamente.

```ts
function showMessages(message: string): void {
	console.log(message)
	return message
}
```

```ts
function showMessages(message: string) {
	console.log(message)
}
```

```ts
function showMessages(message: string) {
	return message
}
```
