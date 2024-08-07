Nesta aula, veremos como incluir CSS no empacotamento usando Webpack. Criaremos uma pasta CSS com um arquivo `styles.css`, aplicando estilos ao `body` e ao`h1`. Vamos configurar o Webpack para lidar com arquivos CSS, instalando os `loaders css-loader` e `style-loader`. Após a configuração, o CSS será empacotado junto com o JavaScript e aplicado corretamente na página HTML.

Dentro da pasta `src` vamos criar uma pasta `css` e um arquivo dentro `styles.css`.

```css
body {
	background-color: #000;
	color: #fff;
}

h1 {
	text-transform: uppercase;
}
```

Agora dentro do nosso `index.js` vamos importar o `css`.

```js
import './css/styles.css'
```

Se rodarmos o `build`, o webpack não vai conseguir lidar com a importação do `css`, então vamos resolver isso, primeiramente instalando o pacote.

```bash
npm install style-loader css-loader --save-dev
```

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
				use: ["style-loader", "css-loader"]
			}
		]
	}
}
```

Agora vamos rodar o `build` e olhar a saída, veremos que não tem um arquivo `css` dentro da `dist`, porque o webpack inclui ele dentro do `css`.

Pra finalizar, o que podemos fazer também, adicionar uma `config` exclude para ele ignorar pastas, como por exemplo a `node_modules`.

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
			}
		]
	}
}
```
