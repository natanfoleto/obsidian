Nesta aula, usaremos o json-server para simular uma API localmente, permitindo concentrar no consumo da API em JavaScript. Aprenderemos a o json-server, criar um arquivo `server.json` com dados simulados e executar o servidor localmente.

Vamos deixar nossa estrutura pronta, `index.html` e `main.js`.

Aqui está o link do GitHub do json-server pra darmos uma olhada: https://github.com/typicode/json-server

O json-server é uma biblioteca/pacote que simula uma API, ela trás os conceitos que acabamos de ver sobre as APIs.

Como ele é um pacote, utilizaremos o `npm` pra instalar. Seguimos então com o comando no terminal.
```bash
npm install json-server
```

Após a instalação, vamos analisar cada arquivos, e pastas criados.

```
node_modules
package.json
package-lock.json
```

Agora vamos criar um arquivo na raiz com nome `server.json` e adicionar um objeto vazio.

```json
{}
```

Agora precisamos criar um `script` para iniciar o nosso servidor utilizando o `json-server`. Faremos isso no `package.json`.

```json
"scripts": {
	"server": "json-server server.json"
}
```

Agora pra testar, vamos abrir o terminal e executar o seguinte comando.

```bash
npm run server
```

Para testar se está tudo certo, podemos abrir o `navegador` e acessar a URL `localhost:3000`.
Neste momento, ainda não existe conteúdo nenhum em nossa API.

Então podemos adicionar conteúdos novos pra testar. Vamos abrir o `server.json`e escrever...

```json
{
	"test": {}
}
```

```json
{
	"test": {
		"name": "Natan Foleto"
	}
}
```

Por padrão a porta que o `json-server` usa em nossa máquina pra disponibilizar nossa API é a `3000`, mas podemos mudar isso caso quisermos. Basta passar uma flag de configuração no script que executa nosso servidor, dentro do `package.json`.

```json
"scripts": {
	"server": "json-server server.json --port=3333"
}
```

Agora precisamos acessar usando a porta `3333`.