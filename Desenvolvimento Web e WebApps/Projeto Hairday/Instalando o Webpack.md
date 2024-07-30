
Vamos começar instalando os pacotes necessários.

```bash
npm i webpack@5.89.0 webpack-cli@5.1.4 --save-dev
```


Agora vamos criar um novo script pro build da nossa aplicação

```json
"scripts": {
	"server": "json-server --watch server.json --port 3333",
	"build": "webpack"
},
```


Agora vamos criar um novo arquivo na pasta `src`, o `main.js`, ele será o nosso entry-point (ponto de entrada).

Logo em seguida vamos criar o arquivo `webpack.confg.js`, onde vamos definir as configuração do webpack.

```js
const path = require("path")

module.exports = {
	target: "web",
	mode: "development",
	entry: path.resolve(__dirname, "src", "main.js"),
	output: {
		filename: "main.js",
		path: path.resolve(__dirname, "dist")
	}
}
```