
Nesta aula, iremos abordar o conceito de acertação de tipo no TypeScript. A acertação de tipo é útil quando o TypeScript não reconhece a tipagem de um objeto, permitindo especificar manualmente o tipo. Foi exemplificado o uso da acertação ao consumir uma API e definir o tipo de retorno. A criação de um tipo personalizado, a sintaxe "as" e a importância da acertação para definir tipos foram destacadas. Este recurso é fundamental para lidar com situações em que o TypeScript não consegue inferir automaticamente o tipo de dados.

```ts
type UserResponse = {
	id: number
	name: string
	avatar: string
}

let userResponse = {} as UserResponse

userResponse.name
userResponse.age
```

