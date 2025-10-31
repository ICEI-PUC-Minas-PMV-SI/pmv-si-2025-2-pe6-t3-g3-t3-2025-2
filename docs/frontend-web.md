# Front-end Web

~~[Inclua uma breve descrição do projeto e seus objetivos.]~~

O Front-end Web da plataforma tem como principal objetivo oferecer uma interface **moderna, intuitiva e responsiva** que facilite a interação entre o usuário e os serviços disponibilizados pela API. O sistema busca proporcionar uma experiência fluida, segura e acessível, permitindo que hóspedes, administradores e gerentes de hotéis interajam com as funcionalidades do sistema de forma simples e eficiente.

## Projeto da Interface Web

~~[Descreva o projeto da interface Web da aplicação, incluindo o design visual, layout das páginas, interações do usuário e outros aspectos relevantes.]~~

O projeto da interface foi elaborado com foco em **usabilidade e experiência do usuário (UX)**, seguindo boas práticas de design responsivo e interatividade. A aplicação foi dividida em módulos visuais correspondentes aos principais fluxos do sistema:

1. **Página Inicial (Home)**:
- Exibe uma barra de pesquisa com filtros de destino, datas e quantidade de hóspedes.
- Mostra seções com destaques, hotéis recomendados e promoções em destaque.
- Inclui um rodapé com links institucionais e informações de contato.

2. **Página de Resultados de Busca**:
- Lista os hotéis filtrados conforme os critérios do usuário.
- Cada item da lista mostra nome, imagem, preço, avaliação e botão “Ver Detalhes”.
- Filtros laterais permitem refinar a busca (por preço, avaliação, comodidades etc.).

3. **Página de Detalhes do Hotel**:
- Exibe imagens em carrossel, descrição completa, tipo de quartos disponíveis e avaliações de outros usuários.
- Contém botões de ação como “Reservar Agora” e “Adicionar aos Favoritos”.

4. **Página de Reserva**:
- Mostra os detalhes do quarto selecionado, datas da estadia e valor total.
- Permite ao usuário confirmar a reserva e selecionar o método de pagamento.
- Inclui mensagens de sucesso e redirecionamento após conclusão.

**Página de Avaliações de Hotéis**:

Sistema CRUD completo para avaliações (criar, editar, excluir)
-Componente de rating interativo com estrelas (1-5)
-Filtro por hotel com dropdown de seleção
-Cards de avaliação mostrando usuário, hotel, rating, comentário
-Controle de permissões - usuários podem editar suas próprias avaliações, admins podem excluir qualquer uma

5. **Área do Usuário (Dashboard)**:
- Exibe as reservas ativas e passadas do usuário.
- Permite editar dados pessoais, cancelar reservas e enviar avaliações.
- Possui controle de autenticação via JWT para proteger as informações.

6. **Painel Administrativo**:
- Exclusivo para usuários com permissão de administrador.
- Permite cadastrar e editar hotéis, quartos e visualizar estatísticas.

### Wireframes

[Inclua os wireframes das páginas principais da interface, mostrando a disposição dos elementos na página.]

**Página de Reservas**

<img width="400" alt="wireframe" src="https://github.com/user-attachments/assets/7141c46a-0eac-4c02-ae32-2c25b9a6d33a" />
<img width="400" alt="wireframe2" src="https://github.com/user-attachments/assets/146e7a82-3f10-426d-a3a2-25001655b419" />


### Design Visual

~~[Descreva o estilo visual da interface, incluindo paleta de cores, tipografia, ícones e outros elementos gráficos.]~~

O design da aplicação foi pensado para oferecer uma experiência agradável, moderna e intuitiva em todos os dispositivos. Utilizando **React Native com Expo**, o objetivo é garantir uma interface **multiplataforma**, funcionando de forma fluida tanto em Android quanto em iOS, a partir de uma única base de código.

O estilo visual segue uma linha **minimalista e funcional**, priorizando clareza e conforto visual. A paleta de cores combina:
- Azul-escuro (**#1E3A8A**) para transmitir confiança
- Amarelo (**#FBBF24**) para destacar ações importantes
- Além de branco (**#FFFFFF**) e cinza-claro (**#F3F4F6**) como base neutra.
<img width="600" alt="Paleta" src="https://github.com/user-attachments/assets/119f77a8-7ad4-4b76-b575-1da4f737153e" />

A **tipografia** principal é *Poppins* (ou *Roboto*, conforme o sistema), com tamanhos e pesos adaptados para boa leitura em telas pequenas.

Os **ícones** seguem um padrão simples e reconhecível, utilizando bibliotecas como Expo Vector Icons, reforçando a usabilidade sem poluir a interface.

O **layout** é responsivo e utiliza Flexbox para ajustar os componentes conforme o tamanho da tela. Animações leves e feedbacks visuais indicam ações do usuário, tornando a navegação mais natural.
A aplicação também segue boas práticas de **acessibilidade**, como contraste adequado e áreas de toque confortáveis, garantindo uma boa experiência para todos os usuários.

## Fluxo de Dados

[Diagrama ou descrição do fluxo de dados na aplicação.]

## Tecnologias Utilizadas
[Lista das tecnologias principais que serão utilizadas no projeto.]

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

Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.

# Planejamento

##  Quadro de tarefas

> Apresente a divisão de tarefas entre os membros do grupo e o acompanhamento da execução, conforme o exemplo abaixo.

Atualizado em: 31/10/2025

| Responsável   | Tarefa/Requisito | Iniciado em    | Prazo      | Status | Terminado em    |
| :----         |    :----         |      :----:    | :----:     | :----: | :----:          |
| AlunaX        | Página inicial   | 01/02/2024     | 07/03/2024 | ✔️    | 05/02/2024      |
| AlunaZ        | CSS unificado    | 03/02/2024     | 10/03/2024 | 📝    |                 |
| AlunoY        | Página de login  | 01/02/2024     | 07/03/2024 | ⌛     |                 |
| Gustavo Rossetti        | Feature Avaliação   |  06/10/25    | 02/11/25 | ✔️    | 31/10/2025      |

Legenda:
- ✔️: terminado
- 📝: em execução
- ⌛: atrasado
- ❌: não iniciado

