
Vamos começar instalando os pacotes necessários.

```bash
npm i webpack-dev-server@4.15.1 --save-dev
```


Agora vamos fazer a configuração do `webpack server` no projeto.

```js
const path = require("path")

module.exports = {
	target: "web",
	mode: "development",
	entry: path.resolve(__dirname, "src", "main.js"),
	output: {
		filename: "main.js",
		path: path.resolve(__dirname, "dist")
	},
	
	devServer: {
		static: {
			directory: path.resolve(__dirname, "dist")
		},
		port: 3000,
		open: true,
		liveReload: true,
	}
}
```


Agora vamos criar um script pra executar o `webpack server`.

```json
"scripts": {
	"build": "webpack",
	"dev": "webpack serve",
	"server": "json-server --watch server.json --port 3333"
},
```