Nesta aula, vamos fazer um experimento para entender a ordem de execução das tarefas no JavaScript, explorando a prioridade do event loop. Este experimento vai proporcionar insights sobre o funcionamento interno do JavaScript.

```js
console.log(1)

queueMicrotask(() => {
	console.log(2)
})

setTimeout(() => {
	console.log(3)
}, 1000)

console.log(4)

Promise.resolve(true).then(() => {
	console.log(5)
})
```

Tendo visto que o `event loop` usa um modelo de concorrência que vimos anteriormente, qual você acha que será a saída desse código?

```js
// (1) Executa o código de forma síncrona, então o valor é mostrado imediatamente no console
console.log(1)

// (3) Microtasks são executadas antes de temporizadores e promessas. 
queueMicrotask(() => {
	console.log(2)
})

// (5) Macrotask que aguarda o evento de temporizados ser acionado. 
setTimeout(() => {
	console.log(3)
}, 1000)

// (2) Execução síncrona. 
console.log(4)

// (4) Adiciona uma microtask. 
Promise.resolve(true).then(() => {
	console.log(5)
})
```