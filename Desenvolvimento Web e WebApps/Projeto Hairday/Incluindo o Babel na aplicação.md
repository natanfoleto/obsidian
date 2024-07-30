
Nesse momento, vamos instalar o `babel` em nossa aplicação, para garantir que nosso app terá compatibilidade com diversos navegadores. Primeiro vamos instalar os pacotes necessários.

```bash
npm i babel-loader@9.1.3 @babel/core@7.23.7 @babel/preset-env@7.23.7 --save-dev
```

Agora vamos voltar ao arquivo `config.webpack.js` para incluir o babel no processo de `build`. Isso fará com que o código gerado pelo `build` seja compatível com diversos navegadores.

```js
rules: [
	{
		test: /\.css$/,
		use: ["style-loader", "css-loader"]
	},
	{
		test: /\.js$/,
		exclude: /node_modules/,
		use: {
			loader: "babel-loader",
			options: {
				presets: ["@babel/preset-env"]
			}
		}
	}
]
```


Vamos testar rodando o comando `npm run build` e depois `npm run dev`.