Nesta aula, aprenderemos a incluir o HTML no pacote gerado pelo Webpack. Utilizaremos o plugin HTML Webpack Plugin, que permite adicionar o HTML na configuração do Webpack. Após a instalação e importação do plugin, vamos configurar no arquivo Webpack.config.js a adição do plugin na seção de Plugins. Ao executar o script `npm run build`, verificaremos que o HTML foi incluído no pacote, juntamente com o JavaScript, facilitando a visualização do conteúdo da aplicação.

Vamos instalar os pacotes necessários pra isso.

```bash
npm i html-webpack-plugin@5.6.0 --save-dev
```

Agora vamos voltar para a configuração do `webpack`.

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
	]
}
```

Agora podemos testar novamente o `build` e visualizar as saídas na pasta `dist`, e abrir o `index.html` direto da `dist`, pra ver se ele vai funcionar normalmente.