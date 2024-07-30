
Se olharmos o resultado do `build`, ainda não temos o `css` e o `favicon` também não foi carregado.

Vamos inclui-lo agora no `build`. Abra o `webpack.config.json` para adicionar essa configuração.

```js
plugins: [
	new HtmlWebpackPlugin({
		template: path.resolve(__dirname, "index.html"),
		favicon: path.resolve(__dirname, "src", "assets", "scissors.svg")
	})
]
```


