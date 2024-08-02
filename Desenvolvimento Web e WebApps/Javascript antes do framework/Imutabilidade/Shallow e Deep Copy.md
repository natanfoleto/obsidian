Nesta aula, abordaremos o conceito de `shallow copy` e `deep copy` em JavaScript. Veremos que a `shallow copy` não copia itens aninhados, enquanto a `deep copy copia tudo`. Veremos exemplos práticos de como realizar cada tipo de cópia e quando é mais adequado utilizá-los. A `deep copy` é recomendada para objetos mais complexos, como arrays e objetos aninhados, para evitar manipulações indesejadas. É importante compreender esses conceitos para evitar problemas de referência em JavaScript.

```js
// Shalow Copy (cópia superficial): não pega os itens aninhados.

const htmlCourse = {
	course: "HTML",
	students: [
		{ name: "Natan", email: "natan@email.com" }
	]
}

const jsCourse = {
	...htmlCourse,
	course: "Javascript"
}

console.log(htmlCourse, jsCourse)
```

```js
// Vai sobreescrever o htmlCouse também, porque students é uma referência
jsCourse.students.push({ name: "João", email: "joao@email.com" })

// Podemos ver que ele criou uma cópia rasa
console.log(htmlCourse, jsCourse)
```

```js
// Deep copy (cópia profunda)

const htmlCourse = {
	course: "HTML",
	students: [
		{ name: "Natan", email: "natan@email.com" }
	]
}

const jsCourse = {
	...htmlCourse,
	course: "Javascript",
	students: [...htmlCOurse.students, { name: "João", email: "joao@email.com" }]
}

jsCourse.students.push({ name: "João", email: "joao@email.com" })

console.log(htmlCourse, jsCourse)
```