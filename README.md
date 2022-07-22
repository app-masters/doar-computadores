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

## 1ª Etapa - Bootstraping

Nesta etapa queremos criar o projeto básico, o mínimo necessário para sairmos do zero.

**Início: 22/07/2022 - envio dos projetos: até 25/07/2022 - resultado: 27/07/2022**   

Tarefas da etapa:   
- Criar projeto backend/frontend seguindo as instruções abaixo (frontend ou backend)
- Criar repositório para seu projeto no github
- Deixar no readme apenas a informação que se trata de um projeto de seleção nosso, com link para nosso site
- Nos enviar a url do seu repositório por [este link](https://programador.emjuizdefora.com/responder/256/) para que possamos avaliar o que foi feito


### Frontend

- Criar projeto usando Next.js
- Na rota inicial, exibir com `<H1>` com "Doação de computadores usados"
- Instalar pacote AXIOS no projeto
- Ao renderizar a interface (apenas uma vez) fazer uma chamada get para [doar-computador-api.herokuapp.com](https://doar-computador-api.herokuapp.com/) e obter a resposta, que será algo como `{alive:true}`
- Se `alive` for `true`, exibir em um `<P>` "API online", se `false` exibir "API offline"

### Backend

O backend será uma API do projeto de doação, que receberá os dados enviados pelos usuários no frontend, e também retornará informações (nas próximas etapas).

- Criar projeto usando Node puro (sem framework) e express
- Ter apenas uma rota GET, a raiz (`/`)
- Na raiz retornar status 200, um objeto json `{alive: true}` (sempre `true`)
- Criar um teste (com jest, superTest, ou [node:test](https://nodejs.org/docs/latest-v18.x/api/test.html)), que faça uma chamada em `/` e dê sucesso caso o resultado seja `{alive: true}`

# Dicas de ouro

- Fique atento a toda informação passada e siga o que foi pedido
- Fazer a menos não é bom, fazer a mais não é necessário nesta primeira etapa
- Estaremos atentos a sua facilidade em seguir as instruções dadas e sua comunicação
- O TypeScript pode ser usado no projeto, mas pode ser o JavaScript sem problema