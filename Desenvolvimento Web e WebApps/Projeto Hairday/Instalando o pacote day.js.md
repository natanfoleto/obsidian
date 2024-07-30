
Vamos adicionar o pacote `day.js`, que traz uma gama de funcionalidades de data e hora em nossa aplicação.

Vamos instalar o pacote usando

```bash
npm i dayjs@1.11.10
```


Agora vamos estruturar o uso dessas bibliotecas de terceiros, vamos criar uma pasta `libs` dentro de `src`, e manteremos as implementações dessas libs por lá.

Agora vamos criar um arquivo `dayjs.js` e adicionar o seguinte código.

```js
import dayjs from "dayjs"
import "dayjs/locale/pt-br"

dayjs.locale("pt-br")
```


Pra utilizar essa configuração do `dayjs` globalmente em nosso projeto, pra cada utilização usar o `dayjs` com a linguagem `pt-br`, vamos ao arquivo `main.js` e adicionar o código abaixo.

```js
// Configuração do dayjs
import "./libs/dayjs.js"
```
