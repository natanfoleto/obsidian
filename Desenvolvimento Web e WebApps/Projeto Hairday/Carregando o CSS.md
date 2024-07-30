
Vamos instalar os pacotes necessários.

```bash
npm i style-loader@3.3.3 css-loader@6.8.1 --save-dev
```

Vamos abrir o ```webpack.config.js``` e adicionar as configurações.

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
			template: path.resolve(__dirname, "index.html"),
			favicon: path.resolve(__dirname, "src", "assets", "scissors.svg"),
		})
	],
	
	module: {
		rules: [
			{
				test: /\.css$/,
				use: ["style-loader", "css-loader"]
			}
		]
	}
}
```


Pra funcionar, ainda precisamos fazer a importação do `css` dentro do arquivo `main.js` na pasta `src`.

```js
"use strict"

import "./styles/global.css"
import "./styles/form.css"
import "./styles/schedule.css"
```

Feito isso, podemos remover o `index.css`, porque ele era o responsável por incluir todos os estilos no HTML. Agora deixaremos pro `webpack` essa responsabilidade.

Outra coisa que também podemos fazer, é remover a `tag` `link:css` do nosso HTML, como dito acima o webpack ja está incluindo o `css` em nosso projeto.