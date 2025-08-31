# Introdução

Viajar e escolher uma hospedagem envolve decisões que vão além da simples disponibilidade de quartos. Informações claras, organizadas e confiáveis sobre acomodações, serviços e localização tornaram-se cada vez mais importantes à medida que o setor de turismo se digitaliza e se torna mais competitivo.

Nesse cenário, os clientes estão cada vez mais bem informados e exigentes, comparando opções, avaliando serviços e buscando experiências que combinem conforto, praticidade e lazer. Atender a essas expectativas exige sistemas capazes de fornecer informações atualizadas e precisas de forma rápida e acessível. As aplicações distribuídas desempenham um papel essencial nesse contexto, permitindo que plataformas digitais escalem para atender simultaneamente múltiplos usuários e estabelecimentos, integrem dados de diferentes fontes e mantenham a disponibilidade e confiabilidade das informações. Dessa forma, elas tornam-se ferramentas estratégicas para conectar clientes e hotéis em um ambiente altamente competitivo e dinâmico, onde a experiência do usuário é um diferencial decisivo.

No entanto, apesar dessas tecnologias, desafios persistem na forma como as informações são apresentadas e consumidas pelos clientes, o que evidencia a necessidade de soluções digitais mais eficazes — exatamente o problema que este projeto busca abordar.

## Problema

O setor de hotelaria e turismo vive um momento de intensa transformação digital, no qual a forma de escolher hospedagens foi profundamente modificada. Se antes esse processo ocorria por meio de contato direto com os estabelecimentos ou visitas presenciais, hoje ele se concentra em plataformas digitais que permitem comparar preços, serviços, avaliações e localizações em poucos cliques. Essa mudança trouxe maior praticidade, mas também revelou uma série de desafios que impactam tanto a experiência do cliente quanto a competitividade das empresas do setor.

Um dos principais obstáculos é a apresentação de informações desorganizadas, desatualizadas ou inconsistentes sobre quartos, preços e serviços. Isso gera insegurança e confusão no processo de escolha, além de situações frustrantes como reservas inválidas ou divergências entre o que foi contratado e o que é efetivamente oferecido no check-in. Para o cliente, esse cenário resulta em perda de tempo, frustração e quebra de confiança em plataformas e estabelecimentos. Para os hotéis, as consequências são igualmente graves: perda de oportunidades de venda, impacto negativo em avaliações públicas e dificuldade em fidelizar hóspedes em um mercado altamente competitivo.

Diante desse contexto, torna-se necessário desenvolver soluções digitais capazes de oferecer informações claras, organizadas e confiáveis, que sustentem uma experiência de busca e reserva transparente, segura e agradável para o usuário final.

## Objetivo geral

Desenvolver uma plataforma digital para o setor hoteleiro que organize e disponibilize informações de forma clara e confiável, proporcionando uma experiência de reserva segura, eficiente e satisfatória para os clientes, ao mesmo tempo em que reduz erros operacionais e melhora a gestão de processos dos hotéis.

### Objetivos específicos

A plataforma deve permitir:

- Cadastro de usuários de forma simples e segura
- Pesquisa de quartos utilizando filtros para facilitar a escolha
- Realização de reservas, com opção de alteração ou cancelamento de acordo com a necessidade do hóspede
- Pagamentos por diferentes meios de forma segura
- Avaliação do serviço após a estadia, garantindo feedbacks confiáveis
- Atualização automática de disponibilidade e informações de quartos, evitando inconsistências e reservas inválidas

## Justificativa

O projeto se justifica pela necessidade de consolidar os conhecimentos adquiridos em semestres anteriores e aplicá-los na criação de uma solução prática e funcional para o setor hoteleiro. A plataforma proposta visa facilitar a experiência de reservas online, oferecendo informações claras, atualizadas e confiáveis sobre quartos, preços e serviços. Dessa forma, é possível reduzir surpresas para os usuários, como indisponibilidade, cobranças inesperadas ou divergências entre o que foi contratado e o que é efetivamente oferecido.

Além de beneficiar os clientes, a solução contribui para a eficiência operacional dos hotéis, organizando processos, integrando dados de diferentes fontes e garantindo maior confiabilidade e agilidade nas operações. Assim, a plataforma não apenas melhora a experiência de busca e reserva, mas também fortalece a competitividade das empresas do setor em um mercado cada vez mais digital e orientado à experiência do usuário.

## Público-Alvo

O principal público-alvo da plataforma são os hóspedes, que apresentam perfis e necessidades distintas durante a estadia. Entre eles estão:

- **Turistas de lazer**, que utilizam o hotel principalmente para descanso enquanto exploram a cidade;
- **Famílias e grupos**, que buscam tanto acomodações confortáveis quanto áreas de lazer disponíveis no hotel;
- **Viajantes a trabalho**, que geralmente têm estadias curtas e utilizam espaços de coworking e serviços voltados para produtividade.

A diversidade de perfis reforça a necessidade de uma plataforma que organize informações de forma clara, permita pesquisas personalizadas e ofereça reservas seguras, atendendo de maneira eficiente às expectativas de cada tipo de hóspede.

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

Atualizado em: 31/08/2025

| Responsável                                  | Tarefa/Requisito                      | Iniciado em |   Prazo    | Status | Terminado em |
| :------------------------------------------- | :------------------------------------ | :---------: | :--------: | :----: | :----------: |
| Matheus Fraga, Victor Henrique               | Introdução                            | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Sibelle Mendes, Matheus Fraga                | Objetivos                             | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Victor Henrique, Matheus Fraga               | Problema                              | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade, Matheus Fraga                  | Justificativa                         | 01/08/2025  | 31/08/2025 |   ✔️    |  05/08/2025  |
| Sibelle Mendes, Matheus Fraga                | Público-Alvo                          | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Sibelle Mendes                               | Histórias de usuário                  | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Sibelle Mendes                               | Mapa de stakeholders                  | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade                                 | Diagramas gerais do projeto           | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade                                 | Arquitetura da Solução                | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade, Matheus Fraga, Victor Henrique | RFs & RNFs                            | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade, Matheus Fraga                  | Solução github action (CI/DC)         | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade, Matheus Fraga                  | Criação do banco de dados             | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Luiz Andrade, Matheus Fraga                  | Hospedagem Azure                      | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Victor Henrique                              | README.md                             | 01/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |
| Matheus Fraga                                | Revisão final de entrega de documento | 29/08/2025  | 31/08/2025 |   ✔️    |  31/08/2025  |

Legenda:

- ✔️: terminado
- 📝: em execução
- ⌛: atrasado
- ❌: não iniciado

