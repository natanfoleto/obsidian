
Nesta aula, veremos diferenças entre `type` e `interface` no TypeScript. Ambos servem para definir tipagens, sendo o `type` mais simples e flexível, enquanto a `interface` é mais utilizada por quem prefere programação orientada a objetos. Mostrei como criar e unir tipos com `type` e `interface`, ressaltando que a escolha entre eles é pessoal, pois ambos cumprem o mesmo propósito. Apesar das sutis diferenças na sintaxe, a proposta é a mesma: definir tipos de dados.

```ts
type TUser = {
	id: number
	name: string
}

type TPayment = {
	method: string
}

// Fazendo união com Type

type TAccount = TUser & TPayment

interface IUser {
	id: number
	name: string
}

interface IPayment {
	method: string
}

// Fazendo união com interfaces
interface IAccount extends IUser, IPayment {}
```
