# Front-end Móvel

~~[Inclua uma breve descrição do projeto e seus objetivos.]~~

O Front-end Móvel da plataforma tem como principal objetivo oferecer uma **interface intuitiva e responsiva** que facilite a interação entre o usuário e os serviços hoteleiros em dispositivos **Android e iOS**. O sistema busca proporcionar uma **experiência fluida, segura e acessível**, permitindo que hóspedes realizem buscas, reservas e avaliações de hotéis de forma prática diretamente de seus smartphones.

## Projeto da Interface
<ins>[Descreva o projeto da interface móvel da aplicação, incluindo o design visual, layout das páginas, interações do usuário e outros aspectos relevantes.]</ins>

### Wireframes

~~[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]~~

<p align="center">
<strong>Finalizar Reserva / Minhas Reservas:</strong><br>
  
<img width="500" alt="wireframes reservas2" src="https://github.com/user-attachments/assets/70ab5481-5a72-4642-b71d-0ebf05e7ba57">
</p>



### Design Visual

~~[Descreva o estilo visual da interface, incluindo paleta de cores, tipografia, ícones e outros elementos gráficos.]~~

O design da aplicação móvel foi desenvolvido para oferecer uma experiência moderna, intuitiva e visualmente agradável em dispositivos móveis. Utilizando **React Native com Expo**, a interface segue princípios de design mobile-first, priorizando **usabilidade, performance e adaptação a diferentes tamanhos de tela**.

A **paleta de cores** foi cuidadosamente selecionada para transmitir confiança, profissionalismo e destacar elementos interativos:

  - **Azul-escuro (#1E3A8A):** Cor primária, utilizada em headers, botões principais e elementos de destaque, transmitindo confiança e estabilidade.
  - **Laranja (#F27F12):** Para destacar ações importantes.
  - **Branco (#FFFFFF):** Background principal, proporcionando clareza e espaçamento visual.
  - **Cinza-claro (#F3F4F6):** Background secundário para separação de seções e cards.
  - **Verde (#10B981):** Feedbacks positivos, confirmações e status "ativo".
  - **Vermelho (#EF4444):** Alertas, erros e ações de cancelamento.
  - **Amarelo (#F59E0B):** Sistema de avaliação (estrelas) e avisos.
<img width="900" alt="paleta" src="https://github.com/user-attachments/assets/3012ca89-dce0-462f-95ac-fbd436c06f27" />


A **tipografia** foi escolhida para garantir uma boa legibilidade em telas pequenas e diferentes resoluções:
 - Poppins / Roboto (conforme o sistema), com tamanhos e pesos adaptados para boa leitura em telas pequenas.
<img width="400" alt="TIPOGRAFIA" src="https://github.com/user-attachments/assets/1277d0d7-2df7-4ce2-a402-a8c9ea3792da" />

Principais **ícones** utilizados:
  - 🏠 Home / Início
  - 🔍 Buscar
  - 📋 Minhas Reservas
  - ⭐ Avaliação
  - 📅 Calendário

## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Tecnologias Utilizadas

~~[Lista das tecnologias principais que serão utilizadas no projeto.]~~

**Frontend:** [React Native + Expo](https://docs.expo.dev/)  
- Permite desenvolvimento multiplataforma (iOS e Android) com uma única base de código.  
- Facilita criação de interfaces responsivas e interativas.

**Backend:** [FastAPI (Python)](https://fastapi.tiangolo.com/)  
- Framework leve e moderno, com suporte nativo a APIs RESTful.  
- Alta performance e facilidade de integração com bancos de dados e autenticação.  

**Mock de sistema de pagamento:** [Beeceptor](https://beeceptor.com/docs/beeceptor-features/)  
- Simula endpoints de pagamento para testes de integração.  
- Permite desenvolvimento e validação do fluxo financeiro sem necessidade de transações reais.

**Tunnel Mmar:** [Mmar](https://github.com/yusuf-musleh/mmar/blob/master/README.md) 
- Plataforma sem dependência que expõe uma URL HTTPS a partir do seu localhost para testes envolvendo cookies.
- Ocultação da porta usada pelo localhost.

## Considerações de Segurança

[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

## Implantação

[Instruções para implantar a aplicação distribuída em um ambiente de produção.]

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.
4. Faça o deploy da aplicação no ambiente escolhido, seguindo as instruções específicas da plataforma de hospedagem.
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

[Descreva a estratégia de teste, incluindo os tipos de teste a serem realizados (unitários, integração, carga, etc.) e as ferramentas a serem utilizadas.]

1. Crie casos de teste para cobrir todos os requisitos funcionais e não funcionais da aplicação.
2. Implemente testes unitários para testar unidades individuais de código, como funções e classes.
3. Realize testes de integração para verificar a interação correta entre os componentes da aplicação.
4. Execute testes de carga para avaliar o desempenho da aplicação sob carga significativa.
5. Utilize ferramentas de teste adequadas, como frameworks de teste e ferramentas de automação de teste, para agilizar o processo de teste.

# Referências

~~Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.~~

1. **Documentação React Native**: https://reactnative.dev/docs/getting-started
2. **Microfundamento: Desenvolvimento de Aplicações Móveis**: Aulas ministradas pelo Prof. Kleber Jacques Ferreira de Souza.
3. **Documentação TailWind CSS**: https://v2.tailwindcss.com/docs
4. **Repositório Mmar**: https://github.com/yusuf-musleh/mmar
5. **Documentação FASTAPI**: https://fastapi.tiangolo.com/#typer-the-fastapi-of-clis
6. **Documentação Python 3.13**: https://docs.python.org/pt-br/3/
7. **Documentação PostgreeSQL**: https://www.postgresql.org/docs/current/index.html

# Planejamento

##  Quadro de tarefas

Atualizado em: 29/11/2025

| Responsável   | Tarefa/Requisito | Iniciado em    | Prazo      | Status | Terminado em    |
| :----         |    :----         |      :----:    | :----:     | :----: | :----:          |
| Victor Pereira, Gustavo Rossetti, Luiz Andrade, Matheus Fraga       | Documentação | 03/11/2025 | 30/11/2025 | ✔️ | 29/11/2025 |
| Matheus Fraga        | Desenvolvimento da feature de Hotéis e Comodidades (versão mobile) | 03/11/2025 | 30/11/2025  | ✔️ | 23/11/2025 |
| Luiz Andrade        | Desenvolvimento da feature de Usuários e Autenticação (versão mobile) | 03/11/2025 | 30/11/2025  | ✔️ | 23/11/2025 |
| Gustavo Rossetti        | Desenvolvimento da feature de Avaliações (versão mobile)  |  03/11/2025 | 30/11/2025 | ✔️ | 23/11/2025 |
| Victor Pereira       | Desenvolvimento da feature de Reservas (versão mobile)  | 03/11/2025 | 30/11/2025 | ✔️ | 23/11/2025 |
| Matheus Fraga        | Testes da Feature de Hotéis e Comodidades (versão mobile)   | 24/11/2025 | 30/11/2025  | ✔️ | 29/11/2025 |
| Luiz Andrade        | Testes da Feature de Usuários e Autenticação (versão mobile) | 24/11/2025 | 30/11/2025  | ✔️ | 29/11/2025 |
| Gustavo Rossetti        | Testes da Feature de Avaliações (versão mobile)  | 24/11/2025 | 30/11/2025 | ✔️    | 29/11/2025 |
| Victor Pereira       | Testes da Feature de Reservas (versão mobile)  | 24/11/2025 | 30/11/2025 | ✔️ | 29/11/2025 |

Legenda:
- ✔️: terminado
- 📝: em execução
- ⌛: atrasado
- ❌: não iniciado

