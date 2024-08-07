Nesta aula, instalaremos o Webpack em uma aplicação, seguindo a convenção de organização de pastas com a pasta "src" para os arquivos criados e a pasta "js" para os arquivos JavaScript. Veremos como criar um arquivo `index.js` e um arquivo `components.js`, e como importar e utilizar esses arquivos no `index.html`.

https://webpack.js.org/

Para mostrar na prática como o `Webpack` funciona, vamos iniciar apenas um `index.html`.

Depois vamos criar uma pasta `src`, e jogar o `index.html` dentro dela. Esta pasta `src` geralmente utilizamos para concentrar o código do nosso projeto. É uma convenção muito utilizada.

Dentro da `src`  uma pasta `js` e dentro dela vamos concentrar nossos arquivos javascript.

Crie um arquivo `index.js` e um arquivo `components.js` dentro de `src/js`. Imagine que esse código cria componentes HTML para nosso site.

```js
export function title(title) {
	const element = document.createElement("h1")
	element.textContent = title

	document.body.appendChild(element)
}
```

Agora no `index.js` vamos importar a função title, e executa-lo passando o valor do título.
Lembrando que pra isso funcionar, precisamos adicionar a tag `script` com type `module` no HTML.

Agora podemos ver que o title é adicionado ao site. Mas vamos remover o `script` do HTML, porque a responsabilidade de empacotar o `js` será do Webpack. Então vamos fazer a instalação do Webpack. Vamos recorrer a doc do webpack pra ver como instalar.

```bash
npm install webpack webpack-cli --save-dev
```

Agora pra executa-lo, no `package.json` vamos criar um `script` pra isso.

```json
"scripts": {
	"build": "webpack ./src/index.js"
}
```

Agora vamos executar `npm run build`, e ver os resultados na pasta `dist`.

