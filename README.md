# Doar Computadores

> Processo de seleção para estágio JavaScript da [App Masters](https://appmasters.io)

Este repositório contem informações sobre o processo de seleção, e será atualizado a cada etapa, seguindo as datas combinadas.

# O Projeto

🎯 O objetivo deste projeto é ajudar pessoas que desejam doar computadores usados, e que estes sejam destinados às pessoas que estejam precisando, ao invés de irem para reciclagem.

Para isso precisamos criar um site/plataforma/sistema por onde o interessado em doar poderá
incluir sua doação, sabendo que se fará bom uso aquele equipamento.

👉 Ao final do processo de seleção, um projeto será publicado em [doarcomputador.com.br](doarcomputador.com.br), e será divulgado para utilização real.

É importante pra nós que todos se divirtam 😄 e aprendam 📚 enquanto estejam no processo conosco. 

# O Processo

O processo acontecerá em 3 ou 4 etapas, com dificuldade crescente, para encontrarmos aqueles estudantes mais animados, interessados e corajosos.

Ao final de cada etapa atualizaremos aqui o repositório com os nicknames dos candidatos que avançaram. A previsão é que o processo todo aconteça em cerca de 12 dias.

Os participantes deverão optar pelo projeto frontend ou backend nas primeiras etapas. Se você se sente fullstack, por agora, terá que optar por um dos lados.

Aqueles que passarem da segunda etapa (para a terceira), estarão concorrendo 🤩 a prêmios como fone de ouvido e um cafeteira Nespresso.

# 1ª Etapa - Bootstraping

Nesta etapa queremos criar o projeto básico, o mínimo necessário para sairmos do zero.

**Início: 22/07/2022 - envio dos projetos: até 25/07/2022 - resultado: 27/07/2022**   

Tarefas da etapa:   
- Criar projeto backend/frontend seguindo as instruções abaixo (frontend ou backend)
- Criar repositório para seu projeto no github
- Deixar no readme apenas a informação que se trata de um projeto de seleção nosso, com link para nosso site
- Nos enviar a url do seu repositório por [este link](https://programador.emjuizdefora.com/responder/256/) para que possamos avaliar o que foi feito


## Frontend

- Criar projeto usando Next.js
- Na rota inicial, exibir com `<H1>` com "Doação de computadores usados"
- Instalar pacote AXIOS no projeto
- Ao renderizar a interface (apenas uma vez) fazer uma chamada get para [doar-computador-api.herokuapp.com](https://doar-computador-api.herokuapp.com/) e obter a resposta, que será algo como `{alive:true}`
- Se `alive` for `true`, exibir em um `<P>` "API online", se `false` exibir "API offline"

## Backend

O backend será uma API do projeto de doação, que receberá os dados enviados pelos usuários no frontend, e também retornará informações (nas próximas etapas).

- Criar projeto usando Node puro (sem framework) e express
- Ter apenas uma rota GET, a raiz (`/`)
- Na raiz retornar status 200, um objeto json `{alive: true}` (sempre `true`)
- Criar um teste (com jest, superTest, ou [node:test](https://nodejs.org/docs/latest-v18.x/api/test.html)), que faça uma chamada em `/` e dê sucesso caso o resultado seja `{alive: true}`

# 1ª Etapa - Aprovados para 2ª etapa

Segue a lista dos 51 candidatos aprovados 🎉 para continuar no processo de seleção 💪 conosco:

- 1uri-silva
- abreuthrj
- Breno Morais
- Brno
- Bruno Jacomini
- Bruno Theodoro
- CaioDamasceno
- CrohnnaroDev
- Daniel Borges
- Daniel Nogueira
- Dienerld
- DittoCujo
- Dubon
- Eduarda Pacheco
- falci
- Felipe Bolzan
- Felipe Rocha
- FillipeF5
- Gabriel Gomes Pena
- gabs_padawan
- gcboaventura
- Gonzaga
- Gustavo C.
- gustavoDekel
- Igor Westermann
- João Silva
- Leonardo Freedy
- Lucas Rocha
- Lucas Zerino
- lucio-iot-dev
- LyonEscalli
- mais do mesmo
- Manuel Cariongo
- MarcioDias
- Maria Fernanda Tavares
- Matheus F
- Matheus ou Magno
- Mazzillio
- McLovin
- padovanilucas
- Patrick
- Patrick Rodrigues
- PedroAugustoACT
- Rafael Coelho
- raphajf
- Rob
- saviorbp
- Thiago Uora
- victor-barros
- Wheeler
- YaghoMattos
- Yan - Refszin

Aos demais agradecemos 🙏 de verdade a participação e esperamos que tenha sido proveitosso de alguma forma este processo.

Caso acredite que seu projeto estava dentro do pedido e deveria ter seguido no processo, entre em contato conosco para conversarmos melhor.

# 2ª Etapa - Formulário e envio dos dados

Nesta etapa queremos criar o formulário para enviar a doação. O doador irá informar quantos equipamentos serão doados, e deverá dar os detalhes de cada um dos equipamentos.

Quem for frontend irá desenvolver a interface de envio, e o back irá lidar com o recebimento dos dados. 

É necessário fazer apenas um deles, não é preciso fazer os dois, ou seja, dê sequencia no seu projeto.

**Início: 27/07/2022 - envio dos projetos: até 31/07/2022 - resultado: 02/08/2022**   

Estrutura dos dados a serem enviados/recebidos.

```
{
    name,
    email,
    phone,
    zip,
    city,
    state,
    streetAddress,
    number,
    complement,
    neighborhood,
    deviceCount,
    devices: [
        {type, condition},
        {type, condition},
        ...
    ]
}
```

Todos campos são obrigatórios (inclusive em `devices`), exceto o endereço de email e complement.

Tarefas da etapa:   
- Implementar sua parte do projeto de seleção
- Ao final das atividades, seguir pelo formulário [neste link](https://programador.emjuizdefora.com/responder/256/) para confirmar suas atividades.

## Frontend

- Criar formulário com duas sessões
- O formulário deve ficar na primeira página, para facilitar a doação
- Manter o projeto usando o Next, ou seja, não implementar o react-router

### Primeira parte, dados pessoais
- A primeira parte recebe os dados pessoais do doador
- Campos de dados pessoais: Nome, e-mail, telefone
- Do endereço, o primeiro campo deverá ser o CEP
- Ao digitar o CEP, exibir um loading enquanto se obtem o endereço
- Caso consiga obter o endereço, preencher os campos e levar o foco para o campo number
- Após estes campos a pessoa irá informar "Quantos equipamentos serão doados"
- Ao informar "1", será exibido abaixo um formulário único formulário de detalhes do equipamento, se "2" então dois formulários, e assim por diante

### Segunda parte, equipamentos
- A segunda parte recebe dados dos equipamentos a serem doados
- Campos dos equipamento para doação: Tipo de equipamento, Estado
- Tipos de equipamento: Notebook, Desktop, Netbook, Monitor, Impressora, Scanner
```
- Notebook - value: notebook
- Desktop - value: desktop
- Netbook - value: netbook
- Monitor - value: screen
- Impressora - value: printer
- Scanner - value: scanner
```
- Estado de conservação (o usuário deverá escolher um deles): 
```
- Tem todas as partes, liga e funciona normalmente - value: working
- Tem todas as partes, mas não liga mais - value: notWorking
- Faltam peças, funciona só as vezes ou está quebrado - value: broken
```

### Envio dos dados
- Enviar os dados (como apresentados acima) via POST para [doar-computador-api.herokuapp.com/donation](https://doar-computador-api.herokuapp.com/donation)
- A API irá falhar com alguma frequência (pra dificultar sua vida), retornando status diferente de `200`. Lide com isso dando feedback ao usuário que o servidor falhar, dizendo algo como "O servidor falhou em responder. Tente mais tarde."
- Ao enviar dados inválidos ou faltando, será retornado o status `400` com detalhes do erro. Lide com isso e dê também o feedback correto ao usuário.

Observação: nossa API só terá esse endpoint no final do dia 27

## Backend

Não é preciso conectar ao banco de dados ainda, apenas lidar com o recebimento dos dados e retorno para o frontend, além de testes bem completos.

### Recebimento dos dados
- Criar rota POST /donation que receberá os dados em um único post
- Se algum campo faltar retornar status `400` com `{error: true, requiredFields: [$field1, $field2, ...], errorMessage: "Todos os campos obrigatórios devem ser informados"}`
- [ ] Validar se o endereço de email é válido
- [ ] Se  a quantidade de itens no array `devices` for diferente de `deviceCount` retornar status `400` com `{error:true, errorMessage: "A quantidade de equipamentos ({$deviceCount}) não está de acordo com as informações de equipamentos enviados ({$sentDevices})"}`
- [ ] Validar se os devices estão chegando com os `types` corretos
- [ ] Se todos os dados estiverem ok, consideraremos que houve sucesso e então retornaremos status `200` com json `{success:true}`

### Testes
- Criar teste para enviar campos faltando, e deverá ter sucesso ao confirmar que a API irá recusar com status `400` e `errorMessage`
- Informar um email inválido, e confirmar que a API recusa com mensagem específica pra isso
- Criar teste para enviar dados pessoais completos, mas não enviar `devices`
- Criar teste que envie dados completos, e `deviceCount` for diferente da quantidade de itens enviados em `devices`, deverá retornar uma falha
- Criar teste que envie um type inválido
- Criar teste que envie dados e devices corretamente, que enfim retornará `200` e `sucess`

Se houver alguma regra que depende de outro teste, ou algum teste que depende de uma regra inexistente, sinta-se a vontade para implementar.

Use o Postman, Insomnia ou outro software parecido para poder ir chamando sua API enquanto desenvolve, para te facilitar validar os retornos.

## Dicas de ouro para a segunda etapa

- Fique atento a toda informação passada e siga o que foi pedido, nomes dos atributos, validações, status, etc
- Fazer a menos será desclassificação, fazer a mais só se for pouco a mais, senão ficará difícil pra gente verificar o que foi realmente feito ou não
- Estaremos atentos a sua facilidade em seguir as instruções dadas e sua comunicação

# 2ª Etapa - Aprovados para 3ª etapa

Todos foram incríveis em seus projetos e foi realmente difícil afunilar o processo, mas foi preciso. Esta é a lista dos 21 candidatos aprovados 🎉 para continuar no processo de seleção 💪 conosco:

- abreuthrj
- Breno Morais
- Bruno Theodoro
- Dienerld
- Douglas_Tott
- Dubon
- falci
- gabs_padawan
- João Silva
- Leonardo Freedy
- lucio-iot-dev
- LyonEscalli
- Maria Fernanda Tavares
- Matheus ou Magno
- Mazzillio
- McLovin
- Patrick
- raphajf
- saviorbp
- Wheeler
- YaghoMattos

Os candidatos que não avançaram, receberão um email com as anotações das observações que fizemos em seus projetos, para fins de feedback, e poder melhorar (se quiser) nestes aspectos.

Faremos um [encontro com todos](#encontro-com-todos); candidatos atuais e os que não estão mais no processo, para conversarmos sobre os erros mais comuns, respondermos perguntas, e darmos algumas dicas para terem mais sucesso nos próximos processos que participarem.


# 3ª Etapa - Back e front juntos

Chegou a hora de trabalhar em equipe, e de ficar mais imerso no ambiente real de desenvolvimento de um projeto.

Nesta etapa back e front terão que conversar, ou seja, um projeto de front irá consumir um projeto de back, de candidatos do próprio processo. Com isso nosso back será desativado.

Entre os que estão nesta etapa, sortearemos 🎲 dois fones de ouvido 🎧 bluetooth. Os vencedores poderão escolher 🤩 entre três modelos diferentes. Mandaremos mais detalhes no grupo do whatsapp nesta semana.

**Início: 02/08/2022 - envio dos projetos: até meia noite de 07/08/2022 - resultado: 10/08/2022**   

O objetivo é validar se você consegue se comunicar bem com outro candidato para tentarem fazer o projeto dar certo, além de evoluir suas atividades individuais.

Quem for do front deverá melhorar seu projeto da forma que achar necessário, além de algumas tarefas extras.

Quem for do back precisará realizar o deploy do seu projeto (para que o front possa ir usando), mas também conectar a um banco de dados para persistir os dados.

Tarefas da etapa:   
- Nos informar quais dias e irá focar mais no projeto [neste link](https://programador.emjuizdefora.com/responder/256/), para encontrarmos um parceiro pra você ainda na terça-feira
- Implementar sua parte do projeto de seleção
- Ao final das atividades, seguir pelo formulário [neste link](https://programador.emjuizdefora.com/responder/256/) (que apresentará outra perguntas) para confirmar suas atividades.

Iremos avaliar as entregas de cada candidato de forma independente, não como um grupo. Mas a integração com a parte de seu parceiro será observada.

## Comunicação

Teremos nove duplas (back/front), onde cada dupla terá um canal exclusivo no nosso slack, com o Tiago Gouvêa, João Baraky, e também o João Bast (frontend) e Bruno Pinheiro (backend) pra te ajudarem e darem suporte.

Conforme formos recebendo as respostas dos dias e horários iremos criando as equipes, e então enviaremos o convite para o slack já para o canal certo. A meta é até o final da terça-feira já termos todos no slack.

Com isso o grupo do whatsapp não será mais necessário pra se comunicar conosco, apenas o slack.

A maioria das empresas de tecnologia utiliza o [Slack](https://slack.com/) para se comunicar internamente, então é bom você já ir se acostumando com ele.

## Daily

Pra gente acompanhar o andamento da sua parte do projeto (e pro outro dev da sua equipe também) você deverá enviar sua daily no canal do slack assim que começar todos os dias (sem hora marcada), respondendo as perguntas:
- O que implementou ontem?
- O que não conseguiu implementar (agarrou) ontem?
- O que irá implementar hoje?
- O que será mais difícil fazer hoje?
- Tem algo te bloqueando de avançar? O que é?

## Frontend

- Ajustar a interface para ficar responsiva, testando como se fosse vista no computador, tablet e celular, em três dimensões no mínimo
- Criar uma lista de instituições que podem receber doações
- Enviar os dados do formulário para o backend do seu parceiro
- Fazer deploy do projeto para o vercel/heroku (ou outro que você prefira)

Quanto a lsita de instituições, crie um menu para ir para esta listagem ou outra forma de acesso para a lista, que deverá estar na rota `/instituicoes`, visto que a pagina inicial ainda é o formulário. Mostre o nome da instituição, cidade, bairro, apresentação breve da instituição, e links para site, instagram, facebook e whatsapp. Crie (no código mesmo) pelo ao menos cinco instituições fictícias (mock) só pra gente ver mesmo, sem nenhuma integração com API nenhuma.

Ao consumir o backend de seu parceiro, eventualmente será necessário fazer alguns ajustes nos retornos e confirmar que tudo continua funcionando. 

Não existirá mais os erros aleatórios forçados na API do seu parceiro, mas, quando der um erro será um problema de verdade, e precisará falar com ele para acharem o problema.

Não queremos que o candidato de back da sua equipe te prejudique, de forma alguma, então observe que nesta etapa você deverá apontar para a API do candidato, porém é uma parte pequena da sua atividade, uma vez que a API dele já deve estar bem parecida com a que você usou na segunda etapa.

Vá avançando nas outras tarefas, inclusive a de deploy, enquanto ele movimenta a parte dele. Se você estiver só dependendo dele, diga na sua daily.

Caso sinta que seu parceiro não está te respondendo a tempo, ou que não dará certo com ele, nos avise (pelo slack mesmo) para te direcionarmos para outro backend (de outro candidato).

# Backend

- Adequar sua API para se comunicar adequadamente com o frontend do seu parceiro
- Adicionar banco de dados no projeto
- Fazer deploy do projeto heroku (ou outro que você prefira)
- Só retornar sucesso se salvar no banco, e objetos que foram salvos (com seus respectivos `id`)
- Usar dotenv, para carregar as informações de conexão com o banco de dados, obtendo do seu .env local, e das configurações de ambiente do heroku (ou outro que você preferir).

Quanto ao banco de dados deverá ser usado mysql ou postgres. Você poderá optar por salvar os dados em duas tabelas (uma para doações e outra pros devices), ou três (incluindo uma pro doador). Caso salve o doador separamente, se o telefone ou email já existir, assumir que o doador é o mesmo.

A pessoa do front dependerá de você, é sempre assim, a galera do front depende do backend pronto. Portanto se você não fez o deploy na segunda etapa, por favor, faça isso antes de mais nada, para que o front já possa consumir sua API e enviar uns posts pra ela e testar a validação.

Se você e seu parceiro de front não derem certo, iremos direcionar vocês pra outros parceiros, ou seja, mudar a dupla. Mas o ideal é que tente dar certo.

# Encontro com todos

Realizaremos na quarta-feira, dia 3 de agosto, as 15h um encontro online via Google Meet e todos estão os que se inscrevera no processo (desde o início) estão convidados.

Conversaremos sobre os erros mais comuns que percebemos, responderemos perguntas, e daremos algumas dicas para terem mais sucesso nos próximos processos que participarem, seja aonde for.

Este é o [link para acesso](https://meet.google.com/eaw-usxg-mzr) ao encontro.

. . . 

🍀 Boa sorte e bons códigos! 🍀