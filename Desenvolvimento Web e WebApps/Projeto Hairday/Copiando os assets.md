
Como o `HTML` e o `CSS`, os assets da aplicação também precisam ser carregados pelo `webpack`. Então vamos instalar os pacotes necessários.

```bash
npm i copy-webpack-plugin@11.0.0 --save-dev
```


Agora vamos pro arquivo de configuração `webpack.config.js`.

```js
const CopyWebpackPlugin = require("copy-webpack-plugin")

...
plugins: [
	new HtmlWebpackPlugin({
		template: path.resolve(__dirname, "index.html"),
		favicon: path.resolve(__dirname, "src", "assets", "scissors.svg"),
	}),
	new CopyWebpackPlugin({
		patterns: [
			{
				from: path.resolve(__dirname, "src", "assets"),
				to: path.resolve(__dirname, "dist", "src", "assets"),
			}
		]
	})
]
```

Vamos rodar `npm run build` pra gerar a `build` do projeto. Caso a pasta não apareça, as vezes um reload no vs-code resolve.