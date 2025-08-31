# Introdução

Viajar e escolher uma hospedagem envolve decisões que vão além da simples disponibilidade de quartos. Informações claras, organizadas e confiáveis sobre acomodações, serviços e localização tornaram-se cada vez mais importantes à medida que o setor de turismo se digitaliza e se torna mais competitivo.

Nesse cenário, os clientes estão cada vez mais bem informados e exigentes, comparando opções, avaliando serviços e buscando experiências que combinem conforto, praticidade e lazer. Atender a essas expectativas exige sistemas capazes de fornecer informações atualizadas e precisas de forma rápida e acessível. As aplicações distribuídas desempenham um papel essencial nesse contexto, permitindo que plataformas digitais escalem para atender simultaneamente múltiplos usuários e estabelecimentos, integrem dados de diferentes fontes e mantenham a disponibilidade e confiabilidade das informações. Dessa forma, elas tornam-se ferramentas estratégicas para conectar clientes e hotéis em um ambiente altamente competitivo e dinâmico, onde a experiência do usuário é um diferencial decisivo.

Este projeto se insere nesse contexto, explorando o papel das aplicações distribuídas no setor de hotelaria, com foco na forma como essas tecnologias podem apoiar serviços digitais modernos e melhorar a experiência geral de busca e seleção de hospedagens.

## Problema

O setor de hotelaria e turismo vive um momento de intensa transformação digital, no qual a forma de escolher hospedagens foi profundamente modificada. Se antes esse processo ocorria por meio de contato direto com os estabelecimentos ou visitas presenciais, hoje ele se concentra em plataformas digitais que permitem comparar preços, serviços, avaliações e localizações em poucos cliques. Essa mudança trouxe maior praticidade, mas também revelou uma série de desafios que impactam tanto a experiência do cliente quanto a competitividade das empresas do setor.

O principal obstáculo está na falta de informações confiáveis e atualizadas sobre disponibilidade de quartos e serviços oferecidos. Em muitos casos, os dados apresentados não estão devidamente padronizados ou integrados, o que gera inconsistências, atrasos e até falhas no momento da reserva. Para o cliente, isso significa insegurança e dificuldade em tomar decisões assertivas; para os estabelecimentos, representa perda de oportunidades de atrair e fidelizar hóspedes em um mercado cada vez mais dinâmico e competitivo.

## Objetivos

Este trabalho tem como objetivo desenvolver uma plataforma que auxilie na otimização do gerenciamenmto de processos no setor de hotelaria, com foco na experiência do cliente, tornando o atendimento mais eficiente, reduzindo erros, economizando tempo, melhorando a qualidade dos serviços e rentabilidade do negócio.

### Objetivos específicos

Elaborar uma plataforma que permita:
- Realizar o cadastro de usuário
- Facilitar a pesquisa de quartos com o uso de filtros
- Permitir a realização de reservas, com opção de alteração ou cancelamento conforme necessidade do hóspede
- Permitir pagamentos por diversos meios
- Possibilitar avaliação do serviço ao final da estadia

## Justificativa

O projeto dá-se principalmente para que haja uma consolidação dos aprendizados e implementação dos conceitos apresentados tanto neste quanto em semestres anteriores, provendo assim uma aplicação estável e segura para utilização. Sendo assim, a principal função do projeto então é facilitar a vida dos usuários que buscam fazer reservas online em um hotel, sendo possível criar a reserva de maneira antecipada e sem surpresas, sejam essas advindas qualquer natureza, como indisponibilidade, taxas abusivas e inconveniências ao longo da estadia.

## Público-Alvo

Os hóspedes são o principal público-alvo do negócio e possuem variados perfis e objetivos durante sua estadia. Os turistas que procuram explorar a cidade e podem utilizar as acomodações somente para descanso, famílias e/ou grupos que além de fazer turismo buscam utilizar as áreas de lazer oferecidas na hospedagem, e pessoas em viagem de trabalho que geralmente têm uma estadia curta mas usufruem dos espaços de coworking nas dependências do hotel. 

## Diagramas de personas
|  Jonathan Santos |
| --- | 
![persona1](img/persona1-jonathan.jpg) 

| Rômulo Andrade |
| --- | 
| ![persona2](img/persona2-romulo.jpg) |

| Madalena Corrêa |
| --- | 
![persona3](img/persona3-madalena.jpg)

| Camila Medeiros |
| --- | 
![persona4](img/persona4-camila.jpg)

## Mapa de stakeholders
![mapa-de-stakeholders](img/mapa-stakeholders-hotel.png)

# Especificações do Projeto

## Requisitos

As tabelas que se seguem apresentam os requisitos funcionais e não funcionais que detalham o escopo do projeto. Para determinar a prioridade de requisitos, aplicar uma técnica de priorização de requisitos e detalhar como a técnica foi aplicada.

### Requisitos Funcionais

|ID    | Descrição do Requisito  | Prioridade |
|------|-----------------------------------------|----|
|RF-001| O usuário deve ser capaz de fazer a reserva de um (ou mais) quartos | ALTA | 
|RF-002| O usuário deve ser capaz de fazer o pagamento com um meio de pagamento a sua escolha  | ALTA |
|RF-003| O usuário deve ser capaz de se cadastrar para utilizar o sistema utilizando seus dados  | ALTA |
|RF-004| O usuário deve ser capaz de realizar pesquisas por quartos do seu interesse  | ALTA |
|RF-005| O usuário deve ser capaz de estender e/ou cancelar sua reserva | ALTA |
|RF-006| O usuário deve ser capaz de filtrar suas buscas  | MÉDIA |
|RF-008| O usuário deve ser capaz de fazer um review (avaliação) de sua estadia | BAIXA |
|RF-009| O sistema impor um padrão de complexidade mínimo exigido às senhas (ao menos uma letra maiúscula, um número e um caractere especial) | ALTA |
|RF-010| O sistema impor uma validade de idade mínima aos usuário durante o cadastro (ao menos 18 anos) | ALTA |
|RF-011| O sistema validar formatação correta de e-mail e número de celular durante o cadastro | ALTA |


### Requisitos não Funcionais

|ID     | Descrição do Requisito  |Prioridade |
|-------|-------------------------|----|
|RNF-001| O sistema deve ser responsivo para rodar em dispositivos móveis nativamente | ALTA | 
|RNF-002| O sistema deve ser responsivo para ser apresentado da maneira correta por telas com resolução variada | ALTA | 
|RNF-003| O sistema deve garantir que os usuários tenham acesso apenas aos dados e funcionalidades compatíveis com seu perfil de permissão | ALTA | 
|RNF-004| O sistema deve implementar autenticação por meio de credenciais (login e senha) com no mínimo 8 caracteres, com combinação mínima de números e caracteres especiais | ALTA |
|RNF-005| Dados sensíveis (como senhas, informações pessoais identificáveis, etc) devem ser armazenados de forma criptografada | ALTA |
|RNF-006| O sistema deve ser hosteado em um ambiente cloud, que permita potênciais surtos de pico de tráfego | MÉDIA | 
|RNF-007| O sistema deve ser apresentado em ao menos duas linguagens (Português e Inglês) | MÉDIA | 

Com base nas Histórias de Usuário, enumere os requisitos da sua solução. Classifique esses requisitos em dois grupos:

- [Requisitos Funcionais
 (RF)](https://pt.wikipedia.org/wiki/Requisito_funcional):
 correspondem a uma funcionalidade que deve estar presente na
  plataforma (ex: cadastro de usuário).
- [Requisitos Não Funcionais
  (RNF)](https://pt.wikipedia.org/wiki/Requisito_n%C3%A3o_funcional):
  correspondem a uma característica técnica, seja de usabilidade,
  desempenho, confiabilidade, segurança ou outro (ex: suporte a
  dispositivos iOS e Android).
Lembre-se que cada requisito deve corresponder à uma e somente uma
característica alvo da sua solução. Além disso, certifique-se de que
todos os aspectos capturados nas Histórias de Usuário foram cobertos.

## Restrições

O projeto está restrito pelos itens apresentados na tabela a seguir.

|ID| Restrição                                             |
|--|-------------------------------------------------------|
|01| O projeto deverá ser entregue até o final do semestre |

Enumere as restrições à sua solução. Lembre-se de que as restrições geralmente limitam a solução candidata.

> **Links Úteis**:
> - [O que são Requisitos Funcionais e Requisitos Não Funcionais?](https://codificar.com.br/requisitos-funcionais-nao-funcionais/)
> - [O que são requisitos funcionais e requisitos não funcionais?](https://analisederequisitos.com.br/requisitos-funcionais-e-requisitos-nao-funcionais-o-que-sao/)

# Catálogo de Serviços

Descreva aqui todos os serviços que serão disponibilizados pelo seu projeto, detalhando suas características e funcionalidades.

# Arquitetura da Solução

Definição de como o software é estruturado em termos dos componentes que fazem parte da solução e do ambiente de hospedagem da aplicação.

![diagrama de arquitetura](img/diagrams/solution-architecture.svg)


## Tecnologias Utilizadas

Backend: [Fastapi (Python)](https://fastapi.tiangolo.com/)

Frontend: [React Native + expo)](https://docs.expo.dev/)

Mock de sistema de pagamento: [Beeceptor](https://beeceptor.com/docs/beeceptor-features/)

## Hospedagem

Hospedagem via Azure web apps + database

# Planejamento

##  Quadro de tarefas

### Etapa 1

Atualizado em: 30/08/2025

| Responsável   | Tarefa/Requisito | Iniciado em    | Prazo      | Status | Terminado em    |
| :----         |    :----         |      :----:    | :----:     | :----: | :----:          |
| Luiz Andrade  | Diagramagem geral                          | 01/02/2024     | 26/02/2024 | ✔️    | 05/08/2025      |
| Luiz Andrade  | Justificativa                              | 01/02/2024     | 26/02/2024 | ✔️    | 05/08/2025      |
| Luiz Andrade  | RFs & RNFs (Parcialmente)                  | 01/02/2024     | 26/02/2024 | ✔️    | 05/08/2025      |
| Luiz Andrade  | Solução github action (Parcialmente)       | 01/02/2024     | 26/02/2024 | ✔️    | 05/08/2025      |
| Luiz Andrade  | Hospedagem Azure (Parcialmente)            | 01/02/2024     | 26/02/2024 | ✔️    | 05/08/2025      |
| Sibelle Diniz | Objetivos                                  | 22/08/2025     | 23/08/2025 | ✔️    | 23/08/2025      |
| Sibelle Diniz | Histórias de usuário                       | 22/08/2025     | 23/08/2025 | ✔️    | 23/08/2025      |
| Sibelle Diniz | Mapa de stakeholders                       | 23/08/2025     | 23/08/2025 | ✔️    | 23/08/2025      |
| AlunoK        | Personas 1  |    01/01/2024        | 12/02/2005 | ❌    |       |

Legenda:
- ✔️: terminado
- 📝: em execução
- ⌛: atrasado
- ❌: não iniciado
