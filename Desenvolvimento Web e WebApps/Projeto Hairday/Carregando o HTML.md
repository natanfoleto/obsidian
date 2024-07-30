
Nesse momento, vamos incluir o HTML na configuração do `webpack`, pra carregar o HTML da nossa aplicação no `build` criado pelo `webpack`.

Vamos instalar os pacotes necessários pra isso.

```bash
npm i html-webpack-plugin@5.6.0 --save-dev
```


Agora vamos voltar para a configuração do `webpack`.

```js
const path = require("path")
const HtmlWebpackPlugin = require("html-webpack-plugin")

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
	},

	plugins: [
		new HtmlWebpackPlugin({
			template: path.resolve(__dirname, "index.html")
		})
	]
}
```

Agora podemos testar novamente o `build`.

