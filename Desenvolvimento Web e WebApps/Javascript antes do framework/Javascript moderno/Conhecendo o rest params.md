Nesta aula, vamos conhecer o operador rest, representado pelos três pontos, que permite receber um número indefinido de argumentos como um array. Vamos aprender a utilizar o rest em uma função para lidar com múltiplos parâmetros dinâmicos. O rest é útil para lidar com situações em que se deseja nomear apenas alguns parâmetros e lidar com o restante de forma flexível. O operador rest é uma ferramenta poderosa para lidar com múltiplos parâmetros de forma eficiente e flexível.

```js
// Rest params (...) permite representar um número indefinido de argumentos como um array.

function values (a, ...rest) {
	console.log(a)
	console.log(...rest)
	console.log(rest)
}

values(2, 1)
values(2, 1, 3, 4)
```