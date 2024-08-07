Nesta aula, abordaremos como automatizar a geração de uma nova build do código, utilizando o Babel. Vamos configurar o script de build no package.json para observar e compilar automaticamente as alterações no código, evitando a necessidade de executar manualmente o script de compilação a cada modificação. Ao adicionar a flag de `watch`, o script fica em constante observação, recompilando o código sempre que houver alterações, mantendo o código atualizado.

Para automatizar o processo de build, vamos atualizar o nosso `script` de build adicionando a flag `--watch`.

```json
"scripts": {
	"build": "babel main.js --watch --out-dir ./dist"
}
```

Ao executar, podemos ver que a mensagem no terminal, diz que ele está em execução e esperando por mudanças.

Vamos atualizar nosso código e ver o que acontece.

