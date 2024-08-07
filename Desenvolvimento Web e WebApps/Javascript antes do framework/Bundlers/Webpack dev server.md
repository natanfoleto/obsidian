Nesta aula, aprenderemos a utilizar o webpack dev server para criar um servidor local e rodar nossa aplicação. Configuraremos o webpack dev server no arquivo `webpack.config.js`, definindo o diretório de entrada, a porta do servidor e a opção de abrir automaticamente o navegador. Com isso, conseguiremos visualizar as alterações em tempo real e facilitar o desenvolvimento da aplicação. O webpack dev server é uma ferramenta útil para o desenvolvimento de aplicações web.

Vamos começar instalando os pacotes necessários.

```bash
npm i webpack-dev-server@4.15.1 --save-dev
```

Agora vamos fazer a configuração do `webpack server` no projeto.

```js
const path = require("path")
const HtmlWebpackPlugin = require("html-webpack-plugin")

module.exports = {
	entry: path.resolve(__dirname, "src", "js", "index.js"),
	output: {
		filename: "main.js",
		path: path.resolve(__dirname, "dist")
	},
	mode: "development",
	plugins: [
		new HtmlWebpackPlugin()
	],
	
	devServer: {
		static: {
			directory: path.resolve(__dirname, "dist")
		},
		port: 3000,
		open: true,
		liveReload: true,
	},
	
	module: {
		rules: [
			{
				test: /\.css$/i,
				use: ["style-loader", "css-loader"],
				exclude: "node_modules"
			},
			{
				test: /\.js$/i,
				exclude: /node_modules/,
				use: {
					loader: "babel-loader",
					options: {
						presets: [
							["@babel/preset-env"], 
							{ 
								targets: "defaults"
							}
						]
					}
				}
			}
		]
	}
}
```

Agora vamos criar um script pra executar o `webpack server`.

```json
"scripts": {
	"build": "webpack",
	"dev": "webpack serve"
},
```

Se modificarmos algo no projeto, ele fará o `build` novamente, sem precisarmos fazer de forma manual. Tudo fica automatizado.