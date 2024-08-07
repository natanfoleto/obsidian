Nesta aula, veremos como instalar e configurar o Babel, um compilador JavaScript amplamente utilizado.

https://babeljs.io/

Vamos instalar o Babel em um projeto cru, com apenas o `index.html` e o `main.js`.

Vamos abrir o terminal e instalar o pacote do Babel. Recomendo sempre usar o guia de instalação da doc do babel.

```bash
npm install --save-dev @babel/core @babel/cli @babel/preset-env
```

Notamos que tem uma flag `--save-dev` no comando, isso indica pro `npm` que essa dependência será instalada como dependência de desenvolvimento.