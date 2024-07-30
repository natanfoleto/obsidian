
No TypeScript, ao não especificar o tipo de uma variável, ela é do tipo "any", aceitando qualquer valor. No entanto, o uso excessivo desse tipo pode causar problemas, indo contra o propósito do TypeScript de evitar erros. O mesmo cuidado se aplica ao definir tipos em funções, onde é preferível especificar tipos específicos, como "number", para evitar resultados inesperados. Evite usar o tipo "any" em variáveis e funções, a menos que seja absolutamente necessário para manter a integridade do código.

```ts
let info: any;

info = [1, 2, 3]
info = 'Rodrigo'
info = true
info = 10.50
```


Outro exemplo:

```ts
function sum(a: any, b: any) {
	return a + b
}

sum(1, 3) // 4
sum("10", 1) // 11
```
