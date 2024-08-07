Na aula, aprenderemos como configurar o Webpack para incluir o Babel, visando garantir a compatibilidade da aplicação com diversos navegadores.

Vamos instalar o babel-loader.

```bash
npm install --save-dev @babel/core @babel/preset-env babel-loader
```

Agora vamos pro `webpack.config.js`.

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

Não se preocupe em decorar tudo isso, a documentação serve pra sempre que precisarmos, podemos olhar. A partir de agora temos o babel configurado em nosso webpack.



