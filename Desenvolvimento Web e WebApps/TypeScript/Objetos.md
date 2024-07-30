
Nesta aula, aprenderemos a criar tipagens para objetos utilizando types em JavaScript, como definir um tipo, como point, com propriedades como eixo x e eixo y, como utilizar essa tipagem ao criar uma função printcord para imprimir coordenadas. Além disso, como criar tipagens para outros objetos. 


```ts
type Point = {
	x: number
	y: number
}

function printCoord(points: Point) {
	console.log(`O eixo x é: ${points.x}`)
	console.log(`O eixo y é: ${points.y}`)
}

printCoord({ x: 101, y: 50 })
```
