Nesta aula, aprenderemos a configurar o Webpack, separando as configurações em um arquivo `webpack.config.js` na raiz do projeto. Vamos definir o arquivo de entrada, as configurações de saída e o modo de desenvolvimento.

Vamos começar mudando o valor do `script` para `webpack` apenas. Pois vamos criar um arquivo de configuração na raiz, o `webpack.config.js` e o comando webpack consegue identifica-lo, e executar a partir das configurações setadas ali.

```js
const path = require("path")

module.exports = {
	entry: "./src/js/index.js",
	output: {
		filename: "main.js",
		path: path.resolve(__dirname, "dist")
	}
}
```

O `path` é um recurso do próprio `node`, que consegue resolver e trabalhar com caminhos em qualquer sistema operacional. Podemos usar o `path` para propriedade `entry` também.

```js
const path = require("path")

module.exports = {
	entry: path.resolve(__dirname, "src", "js", "index.js"),
	output: {
		filename: "main.js",
		path: path.resolve(__dirname, "dist")
	},
	mode: "develoment"
}
```

Agora podemos executar o comando de `build` novamente, e ele executará usando as novas configurações.