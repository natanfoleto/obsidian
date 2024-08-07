Aprenderemos a criar scripts personalizados no arquivo `package.json` para automatizar a compilação do código JavaScript utilizando o Babel. Criaremos um script chamado `build` que executa o Babel para compilar o arquivo `main.js` e salvar na pasta dist. Utilizaremos o comando `npm run build` para executar o script, tornando o processo mais produtivo e eficiente. Essa prática de criar scripts personalizados pode ser aplicada com outros pacotes, facilitando a automação de tarefas nos projetos.

Para começar a prática, vamos criar o novo script para rodar o comando do `babel`.

```json
"scripts": {
	"build": "babel main.js --out-dir ./dist"
}
```

Vamos apagar a pasta `dist` para vermos que quando executarmos o nosso `script build` ele vai gerar a pasta novamente com o código compilado.

```bash
npm run build
```
