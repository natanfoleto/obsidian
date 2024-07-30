
Neste projeto faremos um sistema de agendamento de horários pra uma barbearia ou salão de beleza.

Figma do projeto
https://www.figma.com/design/OkA5FAkbzoYx0aJDYk4SE2/Plataforma-de-agendamento?node-id=0-1&t=Q8Z6KvcfzwM4dJxA-1

## Iniciando o HTML e CSS

Vamos criar o arquivo `index.html` na raiz, e também uma pasta `src`.
Dentro da pasta `src`, vamos criar `assets` e `styles`.

Agora basta criar o código, e quando finalizado vamos para o próximo passo.

## Próximos passos

### Pacotes 

Usando o json-server: [[Usando o json-server]]
Informações da aplicação: [[Informações da aplicação]]
Instalando o Webpack: [[Instalando o Webpack]]
Instalando o Webpack Server: [[Instalando o Webpack Server]]
Carregando o HTML: [[Carregando o HTML]]
Carregando o favicon: [[Carregando o favicon]]
Carregando o CSS: [[Carregando o CSS]]
Copiando os assets: [[Copiando os assets]]
Incluindo o Babel na aplicação: [[Incluindo o Babel na aplicação]]
Instalando o pacote day.js: [[Instalando o pacote day.js]]


### Manipulando o form 

Definindo as horas de atendimento: `utils/opening-hours.js`
Definindo a data atual: `modules/form/submit.js`
Evento de carregamento do conteúdo: `modules/load.js`
Carregando os horários: `modules/schedules/load.js`
Renderizando os horários: `modules/form/hours.load.js`
Separando os horários pelo período
Selecionando um horário: `hours-click.js`
Enviando um horário selecionado para a API
Carregando horários para outros dias: `date-change.js`


### Integração com a API

Criando o api-config: `services/api.config.js`
Criando o serviço de agendamento: `services/schedule-new.js`
Registrando um novo agendamento na API: `modules/form/submit.js`
Serviço para buscar agendamentos do dia: `schedule-fetch-by-day.js`
Buscando os agendamentos na API: `load.js`
Renderizando os agendamentos do dia: `show.js`
Bloqueando horários já agendados: `modules/form/hours.load.js`
Atualizando a lista de agendamentos: `modules/form/submit.js`
Selecionando um agendamento para remover:  `modules/schedules/cancel.js`
Removendo um agendamento da API: `services/schedule-cancel.js`



