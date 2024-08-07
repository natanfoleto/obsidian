Neste momento, veremos a importância do arquivo `babel.config.js`, que influencia o comportamento do Babel. A ideia é mostrar que é possível configurar o Babel de acordo com as necessidades do projeto.

Vamos configurar os targets, pra dizer quais navegadores eu quero o meu código `js` de suporte.

```js
const presets = [
	[
		"@babel/preset-env",
		{
			targets: {
				edge: "17",
				firefox: "60",
				chrome: "60",
				safari: "11.1"
			}
		}
	]
]

module.exports = { presets }
```

Dessa forma nosso código funcionará pra essas versões desses navegadores.

Vamos criar um `script: dev` pra ter duas opções de execução, o `build` manual, pra executar quando eu quiser, e o `build` automático quando eu tiver desenvolvendo o código.

```json
"scripts": {
	"build": "babel main.js --out-dir ./dist",
	"dev": "babel main.js --watch --out-dir ./dist"
}
```

Agora quando eu quiser rodar o `build` sem travar o terminal, eu uso o script `build`, e quando eu tiver desenvolvendo utilizo o `dev`, pra ele ir buildando o código automaticamente.