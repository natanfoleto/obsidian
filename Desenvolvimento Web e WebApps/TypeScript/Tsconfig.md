
O TypeScript utiliza o arquivo tsconfig para configurar as regras do projeto, como tipagem de parâmetros de funções. No TypeScript Playground, é possível ajustar as configurações do tsconfig, como desabilitar alertas de tipos implícitos. É importante definir explicitamente os tipos para evitar erros. O tsconfig permite configurar várias opções, como linguagem, versão do JavaScript e frameworks como React. Focar em entender a importância e funcionalidades do tsconfig é fundamental para configurar projetos em TypeScript.

Quando estamos usando TS, vai existir um arquivo `tsconfig.json` em nosso projeto
Lá estará todos as regras que o nosso Typescript deve seguir
  
Por exemplo, quando eu crio a função sum()
```ts
function sum(a, b) {}
```
  
Esse código apontaria um erro falando que eu não posso deixar a e b sem tipos
Nas configurações do `tsconfig` eu poderia desativar essa regra.