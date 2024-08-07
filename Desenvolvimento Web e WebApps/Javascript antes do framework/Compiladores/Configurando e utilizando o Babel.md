Vamos configurar e executar o Babel em nosso projeto. Criaremos o arquivo `babel.config.js` na raiz do projeto, configuraremos os presets e exportaremos as configurações. Em seguida, executaremos o Babel no terminal, compilando o arquivo `main.js` para a pasta dist. Demonstraremos a transformação do código ECMAScript 2015 em um formato suportado pelos navegadores.

Vamos criar o arquivo `babel.config.js` na raiz. O nome precisa ser exatamente esse, pois o babel vai identifica-lo pra ler as configurações que desejamos setar para ele.

```js
const presets = ["@babel/preset-env"]

module.exports = { presets }
```

Após a configuração, podemos executar o seguinte comando.

```bash
./node_modules/.bin/babel main.js --out-dir dist
```

Vamos ver o resultado disso na pasta de saída `dir`. Como não tinha nada em `main.js`o babel praticamente não converteu nada, vamos ao arquivo `main.js`e escrever alguns códigos pra testar novamente.

```js
class User {
	constructor({ email }) {
		this.email = email
	}
}

let user = new User({ email: "natanfoleto@email.com" })
```

Agora vamos executar o babel novamente, e ver os resultados em `dist`. E ao visualizar podemos ver que teremos um monte de código compilado, de uma forma que dará suporte a todos navegadores.

