Nesta aula, veremos como utilizar o day.js em um projeto, mostrando a importância de consultar a documentação para entender as funcionalidades disponíveis. Vamos aprender como inserir o pacote no projeto e como utilizar as funcionalidades do day.js, como formatar datas e horas. A exploração da documentação é uma prática essencial para aproveitar ao máximo as bibliotecas e pacotes, facilitando o desenvolvimento e evitando a necessidade de criar funcionalidades do zero.


Vamos iniciar com uma estrutura simples, usando um `index.html` e `main.js`.

Vamos abrir novamente a documentação do `dayjs`, e procurar a parte de instalação. Vamos inclui-lo em nosso projeto utilizando a forma `Browser`, que nos da um `<script>` que trará a biblioteca pra dentro do nosso projeto.

```html
<!-- CDN example (jsDelivr) --> 
<script src="https://cdn.jsdelivr.net/npm/dayjs@1/dayjs.min.js"></script> 
```

Feito a importação, podemos utilizar em nosso projeto. Vamos ao `main.js`

```js
const now = dayjs()

console.log(now)

// Ou exibir formatada
console.log(now.format('DD/MM - HH:mm'))
```