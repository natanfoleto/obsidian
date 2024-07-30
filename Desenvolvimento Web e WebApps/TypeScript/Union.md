
Vamos utilizar operador de union do TypeScript, mostrando como criar uma função chamada printUserId que pode aceitar diferentes tipos de dados, como number ou string. Utilizando o operador de union (|), podemos indicar que uma variável pode aceitar mais de um tipo de dado. Isso permite maior flexibilidade ao definir os tipos de dados que uma variável pode armazenar. O uso desse operador é fundamental para lidar com diferentes tipos de dados em TypeScript.

```ts
function printUserId(id: string | number) {
	console.log(`O ID do usuário é ${id}`)
}

printUserId('101')
printUserId(10)
```
