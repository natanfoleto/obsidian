Nesta aula, vamos aprender sobre o modo estrito do JavaScript, conhecido como `strict mode`, que ao ser ativado, torna os erros que eram silenciosos em exceções. Vamos ver como o modo estrito pode ajudar a identificar erros, como a questão de variáveis não definidas e parâmetros duplicados em funções. O uso do `strict mode` é recomendado para evitar problemas comuns de flexibilidade do JavaScript, garantindo um código mais robusto e correto.

```js
// O stric mode (modo estrito): ativando esse modo, os erros que eram silenciosos passa a gerar exceções no Javascript.
"use strict"

function showMessage() {
	"use strict"
	
	personName = "Natan Foleto"
	
	console.log("Olá", personName)
}

showMessage()

class Students {
	get point() {
		return 7
	}
}

let student = new Student()

student.point = 10
```