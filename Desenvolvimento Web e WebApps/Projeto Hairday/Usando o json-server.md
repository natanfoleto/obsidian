Vamos começar instalando o primeiro pacote, o json-server

```bash
npm i json-server@1.0.0-alpha.21
```

Este comando criará a pasta node_modules na raiz do projeto

Se estivermos utilizando o git, vamos adicionar um arquivo `.gitignore` na raiz do projeto, pra ele ignorar algumas pastas e arquivos indesejados.

```
node_modules
```


Agora vamos criar o arquivo `server.json` na raiz, que será nossa API nesse projeto.

```json
{
	"schedules": []
}
```


Agora vamos criar o script `server` do nosso projeto em `packge.json`.

```json
{
	"scripts": {
		"server": "json-server --watch server.json --port 3333"
	},
	"dependencies": {
		"json-server": "^1.0.0-alpha.21"
	}
}
```

O script `server` fará com que rodamos o `json-server` no arquivo `server.json` na porta `3333`, a flag `--watch` faz com que qualquer mudança que tenha no `server.json`, ele recarregue automaticamente o servidor.