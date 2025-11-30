# Front-end Móvel

O Front-end Móvel da plataforma tem como principal objetivo oferecer uma **interface intuitiva e responsiva** que facilite a interação entre o usuário e os serviços hoteleiros em dispositivos **Android e iOS**. O sistema busca proporcionar uma **experiência fluida, segura e acessível**, permitindo que hóspedes realizem buscas, reservas e avaliações de hotéis de forma prática diretamente de seus smartphones.

## Projeto da Interface

A interface móvel foi projetada para oferecer uma navegação simples, visualmente consistente e otimizada para dispositivos Android e iOS. **O layout segue princípios de design centrado no usuário**, priorizando clareza, acessibilidade e fluidez durante o uso.

A navegação é organizada em abas inferiores e fluxos internos, permitindo fácil acesso às principais funcionalidades: página inicial, busca de hotéis, reservas e avaliações. **As telas utilizam componentes padronizados, como cards e botões destacados**, garantindo uniformidade visual e, consequentemente, melhor entendimento para o usuário.

As interações foram desenvolvidas para serem intuitivas, com feedbacks visuais, validação de campos, etc. O objetivo é proporcionar uma experiência agradável, responsiva e eficiente em todas as etapas da jornada do usuário.

### Wireframes

<p align="center">
<strong>Página Inicial (deslogado) / Página Inicial (logado)</strong><br>
  
<img width="500" alt="homepage" src="https://github.com/user-attachments/assets/a329eb42-5e48-4406-a33b-6596513e6860" />
</p>

---

<p align="center">
<strong>Cadastro de Usuário / Configurações de Usuário</strong><br>
  
<img width="500" alt="cadastro e configs de users" src="https://github.com/user-attachments/assets/03794709-f314-410c-8076-809f74eb1f26" />
</p>

---

<p align="center">
<strong>Finalizar Reserva / Minhas Reservas</strong><br>
  
<img width="500" alt="wireframes reservas2" src="https://github.com/user-attachments/assets/70ab5481-5a72-4642-b71d-0ebf05e7ba57">
</p>

---

<p align="center">
<strong>Cadastro de Hotéis</strong><br>
  
<img width="250" alt="Cadastro de Hotel" src="https://github.com/user-attachments/assets/3cc98289-68cc-4137-9a72-6e167acf2004" />
</p>

---

<p align="center">
<strong>Avaliações (Reviews)</strong><br>

<img width="250" alt="Reviews" src="https://github.com/user-attachments/assets/47002bcd-1d3d-4bf5-9d73-a5a0dc320fda" />
</p>

### Design Visual

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

O diagrama de arquitetura abaixo foi desenvolvido com base no **estilo arquitetural baseado em serviços (SOA - Service-Oriented Architecture)**. Esse estilo foi escolhido para garantir:

  - **Desacoplamento** entre módulos, facilitando alterações futuras.
  - **Manutenabilidade**, permitindo atualização ou substituição de componentes sem afetar todo o sistema.
  - **Extensibilidade**, possibilitando a inclusão de novos serviços conforme o crescimento do projeto.
  - **Segurança e robustez**, assegurando que os dados dos usuários e transações sejam protegidos.
  - **Experiência do usuário de qualidade**, com respostas rápidas e confiáveis.

![diagrama de arquitetura](img/diagrams/solution-architecture.svg)

  O sistema é dividido em três camadas principais:

  1. **Frontend**: Responsável pela interface do usuário, interação e captura de dados.
  2. **Backend**: Processamento das regras de negócio, gerenciamento de reservas, autenticação, pagamentos e serviços relacionados.
  3. **Banco de Dados**: Armazenamento de informações persistentes, incluindo usuários, reservas, hotéis e transações.

## Tecnologias Utilizadas

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

A segurança é um aspecto essencial no desenvolvimento da plataforma de gestão hoteleira distribuída, especialmente por lidar com dados sensíveis de usuários, reservas e transações financeiras. As principais considerações de segurança adotadas no sistema incluem:

1. **Autenticação e Autorização**:
O acesso aos recursos protegidos da API é controlado por meio de tokens JWT (JSON Web Tokens) e Cookies. Cada usuário autenticado recebe um token que contém informações de identificação e permissões, garantindo que apenas usuários autorizados possam realizar operações específicas, como criação, edição ou exclusão de reservas e avaliações.

2. **Criptografia de Senhas**:
As senhas dos usuários são criptografadas utilizando a biblioteca bcrypt, implementada através do pacote Passlib, antes de serem armazenadas no banco de dados. Isso impede que senhas sejam lidas mesmo em caso de vazamento de dados.

3. **Proteção de Rotas (Front-end + Backend)**
Tanto o front-end quanto o backend implementam mecanismos que bloqueiam o acesso não autorizado a telas e endpoints protegidos. Esse mecanismo impede que usuários acessem páginas ou dados restritos, mesmo que tentem navegar diretamente por URL ou manipular o aplicativo.

   - <ins>No Backend</ins>: Rotas críticas somente podem ser acessadas quando o token JWT é validado. Caso o token seja inválido ou expirado, a requisição é imediatamente rejeitada com código 401 (Unauthorized).
   - <ins>No Front-end</ins>: Cada tela sensível (como Minhas Reservas, Finalizar Reserva e Avaliações) é protegida por middlewares/guards que verificam a existência de um token ativo. Usuários não autenticados são automaticamente redirecionados para a tela de login.

4. **Proteção contra ataques comuns**:
O sistema adota práticas de mitigação contra ataques frequentes em aplicações web:
   - <ins>SQL Injection</ins>: as interações com o banco são realizadas via SQLAlchemy ORM, que abstrai as queries e evita injeções diretas.
   - <ins>Cross-Site Scripting (XSS)</ins>: validações rigorosas nos campos de entrada, utilizando Pydantic, impedem a inserção de scripts maliciosos.

5. **Comunicação Segura**:
Todas as requisições devem trafegar sob o protocolo HTTPS, garantindo a criptografia ponta a ponta dos dados enviados e recebidos entre clientes e servidores.

6. **Logs e Monitoramento**:
A API mantém registros de ações críticas, como tentativas de login, criação e cancelamento de reservas, e exclusões de dados. Isso permite rastrear atividades suspeitas e auditar o comportamento dos usuários e administradores.

7. **Controle de Acesso e Permissões**:
Usuários comuns têm acesso apenas aos recursos pessoais (como suas próprias reservas e avaliações), enquanto administradores possuem privilégios adicionais, como gerenciar hotéis e quartos. Essa separação garante o princípio do menor privilégio.

## Implantação

A implantação da aplicação envolve a preparação do ambiente backend, configuração do app mobile e disponibilização do sistema para testes ou produção. Como o frontend é desenvolvido em **React Native com Expo**, o processo inclui também o uso do Expo Go e do QR Code gerado pelo Expo CLI para facilitar execução e validação em dispositivos móveis.

### 1. Requisitos de Hardware e Software
- Hardware mínimo para o servidor (Backend):
  - CPU: 2 vCPUs
  - Memória RAM: 4 GB
  - Armazenamento: 20 GB SSD
  - Conectividade: acesso à internet estável, com as portas 8000 (API) e 5432 (PostgreSQL) liberadas

- Software necessário no servidor:
  - Sistema operacional: Ubuntu Server 22.04 LTS (ou equivalente Linux)
  - Python: versão 3.13 ou superior
  - PostgreSQL: versão 15 ou superior
  - Git: controle de versão e integração contínua
  - MMAR: utilizado apenas em ambiente de desenvolvimento para expor o servidor local publicamente e facilitar testes com o frontend.
 
- No Frontend (máquina do desenvolvedor):
  - Node.js 18+
  - Expo CLI
  - Expo Go (instalado no smartphone Android/iOS)

***

### 2. Plataforma de Hospedagem

Pode ser implantado em plataformas como:
  - Render
  - Railway
  - AWS
  - Google Cloud
  - DigitalOcean
  - Azure
  - Para ambientes de teste ou projetos menores, um VPS simples é suficiente.
  - O frontend mobile não é hospedado como um site — ele é executado via Expo Go durante desenvolvimento e pode ser distribuído via build (APK, AAB ou IPA) caso necessário.

***

### 3.1 Configuração do Ambiente Backend

  - Clonar o repositório:
    
  `git clone https://github.com/matheusfraga-tech/aluga-api-backend.git`
  
  `cd aluga-api-backend`

  - Configurar variáveis de ambiente:
  Crie um arquivo .env na raiz do projeto com os dados de conexão:

`DATABASE_URL=postgresql+psycopg2://usuario:senha@localhost:5432/nome_do_banco`

`SECRET_KEY=sua_chave_secreta`

`EXPO_PUBLIC_API_URL=https://sua-api-em-producao.com`

  - Instalar dependências:

`python -m venv .venv`

`source .venv/bin/activate`

`pip install -r requirements.txt`

### 3.2 Configuração do Ambiente Frontend

  - Clonar o repositório:
    
  `git clone https://github.com/Andradev101/aluga-api-frontend.git`
  
  `cd aluga-api-frontend`

***

### 4. Deploy da Aplicação

**Backend (FastAPI)**

- Fazer o build e iniciar o servidor Uvicorn com:

   `fastapi dev app/main.py`
  
*O servidor Uvicorn executará a aplicação na porta 8000.*

**MMAR**:

- Rode o MMAR através do seguinte comando no CMD:
`mmar.exe client --local-port 8000`

**Frontend (Expo / React Native)**

Certifique-se de configurar:
  - .env com: EXPO_PUBLIC_API_URL="link gerado no MMAR"

Inicie o app localmente:

`npm install`

e depois

`npx expo start`

*O Expo CLI abrirá o painel no navegador, permitindo rodar o app no Android Emulator, iOS Simulator ou Expo Go (via QR Code).*

***

### 5. Testes Pós-Implantação

**Testando no Celular com Expo Go (via QR Code)**

1. Instale o app Expo Go no smartphone (Android ou iOS).
2. Com o Expo CLI rodando, a página exibirá um QR Code.
3. No Android: basta abrir a câmera ou o próprio Expo Go e escanear o QR Code.
4. No iOS: o leitor de QR Code da câmera pode ser usado diretamente.
5. O Expo Go carregará o app imediatamente, consumindo a API configurada em EXPO_PUBLIC_API_URL.

## Testes

<details>
<summary><strong>🔐 TESTES DE REGISTRO</strong></summary>

<br>

<details>
<summary><strong>✅ Registro com informações válidas</strong></summary>

<br>

- Na página inicial, clicar em <strong>Sign Up</strong>.
- Preencher um nome de usuário que não exista ainda.
- Preencher uma senha com, no mínimo 8 caracteres, devendo incluir uma letra, um número e um símbolo.
- Selecionar uma data de nascimento que seja correspondente a uma pessoa maior de 18 anos.
- Preencher um email válido.
- Digitar um número de telefone válido.
- Preencher um nome.
- Preencher um sobrenome.
- Preencher um endereço.

**Evidências**:

<img width="200" alt="registro1" src="https://github.com/user-attachments/assets/8f8bbee8-03ac-4772-aca3-f317e92bcbb5" />

<img alt="registro2" src="https://github.com/user-attachments/assets/0b10e6f0-f306-4423-8aa4-7576ddc4f791" />


</details>

<details>
<summary><strong>❌ Registro com informações inválidas</strong></summary>

<br>

- Na página inicial, clicar em <strong>Sign Up</strong>.
- Todos os campos devem estar preenchidos, caso contrário aparecerão avisos.
- O usuário deve selecionar uma data de nascimento que seja correspondente a uma pessoa maior de 18 anos, caso contrário, aparecerá um aviso.
- O usuário deve preencher um email corretamente, caso contrário, aparecerá um aviso.
- O usuário deve preencher um número de telefone válido, caso contrário, aparecerá um aviso.

**Evidências**:

<img width="200" alt="registro3" src="https://github.com/user-attachments/assets/a1f711d4-a965-4cc2-bdf6-8166f3c6824f" />

<img width="200" alt="registro4" src="https://github.com/user-attachments/assets/042090d2-661c-4bc7-b62a-4663feaf0994" />

<img width="200" alt="registro5" src="https://github.com/user-attachments/assets/e4dbde4b-54ae-4ad9-a81b-187ed1a8e45e" />

<img width="200" alt="registro6" src="https://github.com/user-attachments/assets/2e1e8588-49b6-4d9d-bac2-4699f2d1beb6" />

</details>

</details>

<br>

<details>
<summary><strong>🔑 TESTES DE LOGIN</strong></summary>

<br>

<details>
<summary><strong>✅ Login com informações válidas</strong></summary>

<br>

- Na página inicial, navegando até a parte de **Login**.
- O usuário preenche o seu username criado corretamente.
- O usuário preenche a sua senha escolhida para o username corretamente.
- O usuário clica no botão de **Login**.
- Ele é redirecionado para a página inicial da aplicação.


**Evidências**:

![login1](https://github.com/user-attachments/assets/cfcddc97-9546-420a-9f86-15d3e1d66392)

<img width="800" alt="login1" src="https://github.com/user-attachments/assets/717a6406-d4b7-499f-b8c4-ac9f2074116b" />


</details>

<details>
<summary><strong>❌ Login com informações inválidas</strong></summary>

<br>

- Na página inicial, navegando até a parte de Login.
- O usuário preenche um username que não existe.
- O usuário preenche a senha incorretamente.
- O usuário clica no botão de **Login**.
- Um aviso em vermelho aparece indicando o erro.


**Evidências**:

<img width="400" alt="loginerro1" src="https://github.com/user-attachments/assets/b14e5428-c2f9-4135-ae9c-d54e8cfdcd8d" />

<img width="390" alt="loginerro2" src="https://github.com/user-attachments/assets/1600485e-d5a0-4054-a74a-30b350d6772e" />

</details>

</details>

<br>

<details>
<summary><strong>🛏️ TESTES DE RESERVA</strong></summary>

<br>

<details>
<summary><strong>📱 Reserva via PIX</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar um dos hotéis** a partir da busca.
- Na tela seguinte, deve clicar no botão **Reservar Agora**.
- Na tela seguinte, ele deve escolher o **tipo do quarto** que deseja.
- Em seguida, selecionar as **datas da estadia**.
- Depois disso, escolher o **método de pagamento PIX**.
- Marcar que leu e aceita os **Termos e Condições**.
- Clicar em **Confirmar Reserva**.
- Ele será redirecionado para uma tela informando que a Reserva foi Confirmada e com os Detalhes da Reserva.


**Evidências**:

<img width="400" alt="reserva1" src="https://github.com/user-attachments/assets/6122e782-9281-4b58-8095-61bfb53680e9" />

<img width="1000" alt="reserva2" src="https://github.com/user-attachments/assets/7b5d9925-1bee-4c3f-8e2e-e68abff65c3d" />

</details>

<details>
<summary><strong>💳 Reserva via Cartão de Crédito/Débito</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar um dos hotéis** a partir da busca.
- Na tela seguinte, deve clicar no botão **Reservar Agora**.
- Na tela seguinte, ele deve escolher o **tipo do quarto** que deseja.
- Em seguida, selecionar as **datas da estadia**.
- Depois disso, escolher o **método de pagamento Cartão de Crédito/Débito**.
- Preencher corretamente o número do cartão, nome no cartão, data de validade e CVV.
- Marcar que leu e aceita os **Termos e Condições**.
- Clicar em **Confirmar Reserva**.
- Ele será redirecionado para uma tela informando que a Reserva foi Confirmada e com os Detalhes da Reserva.


**Evidências**:

<img width="400" alt="reserva3" src="https://github.com/user-attachments/assets/a42f29d6-91f4-47a1-9759-0eb708632e71" />

<img width="1000" alt="reserva4" src="https://github.com/user-attachments/assets/73f9bcd0-2532-4586-9422-e06e4ed35d4d" />

</details>

<details>
<summary><strong>❌ Reserva com Informações Incorretas</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar um dos hotéis** a partir da busca.
- Na tela seguinte, deve clicar no botão **Reservar Agora**.
- Na tela de finalizar reserva, o usuário deve obrigatoriamente selecionar um quarto disponível, caso contrário avisos aparecerão.
- O usuário deve, obrigatoriamente, selecionar uma data válida, caso contrário avisos aparecerão.
- O usuário também deve, obrigatoriamente, preencher os campos do cartão, caso seja o modelo escolhido. Caso contrário, a reserva não é efetuada.
- O usuário deve declarar que leu os Termos e Condições, caso contrário, o botão de Confirmar fica desabilitado.


**Evidências**:

<img width="400" alt="reserva5" src="https://github.com/user-attachments/assets/4b8f9a3f-b791-4cbe-8100-44aa12303cdb" />

</details>

</details>

<br>

<details>
<summary><strong>⭐ TESTES DE AVALIAÇÕES</strong></summary>

<br>

<details>
<summary><strong>📝 Criar Avaliação de Hotel</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar a aba de Avaliações** no canto inferior da página inicial.
- Na tela seguinte, deve clicar no botão **Avaliar Hotel**.
- Em seguida, ele deve selecionar o hotel que deseja fazer a avaliação.
- Selecionar a quantidade correspondente de estrelas que deseja dar para o hotel.
- Depois disso, escrever um comentário sobre o hotel.
- Clicar em **Criar Avaliação**.
- Após isso, ele será redirecionado para a página de Minhas Avaliações onde poderá visualizar as avaliações criadas.

**Evidências**:

<img width="1000" alt="avaliacao1" src="https://github.com/user-attachments/assets/76ec6165-17d8-4871-bb6b-39c48214c364" />

<img width="1000" alt="avaliacao2" src="https://github.com/user-attachments/assets/c1a2f247-2d71-4f05-a32a-fd432e4e3ac1" />

</details>

<details>
<summary><strong>✏️ Editar Avaliação</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar a aba de Avaliações** no canto inferior da página inicial.
- Na tela seguinte, deve escolher a avaliação que deseja editar.
- Em seguida, o usuário pode alterar o que desejar.
- Depois ele deve clicar em **Update**.

**Evidências**:

<img width="1000" alt="avaliacao3" src="https://github.com/user-attachments/assets/370c59ec-16a4-498f-9a74-0c2e48dc8ed2" />

<img width="1000" alt="avaliacao4" src="https://github.com/user-attachments/assets/bd6b8cf1-60b4-428b-9ac3-e512410baf81" />

</details>

<details>
<summary><strong>❌ Deletar Avaliação</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar a aba de Avaliações** no canto inferior da página inicial.
- Na tela seguinte, deve escolher a avaliação que deseja deletar.
- Em seguida, deve clicar em **Delete**.
- A avaliação desaparecerá e a página de Minhas Avaliações será carregada sem ela.

**Evidências**:

<img width="1000" alt="avaliacao5" src="https://github.com/user-attachments/assets/f07cbe63-0ca5-4f95-80ee-01ebcd4557e8" />

<img width="1000" alt="avaliacao6" src="https://github.com/user-attachments/assets/24bf9428-6171-400e-a191-334c938f2af7" />

</details>

</details>

<br>

<details>
<summary><strong>🏨 TESTES DE CADASTRO DE HOTÉIS</strong></summary>

<br>

<details>
<summary><strong>✅ Cadastro de Hotel com Informações Válidas</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar a aba Perfil** no canto inferior da página inicial.
- Deve selecionar a opção **Cadastrar Novo Hotel** na parte de Ações Administrativas.
- Na tela seguinte, deve preencher as informações do Hotel a ser cadastrado. Todas com asteriscos são obrigatórias.
- Após o preenchimento, o usuário clica em **Cadastrar Hotel no Catálogo**.
- O hotel é cadastrado e é possível buscá-lo na lista com os demais.

**Evidências**:

<img width="1000" alt="hoteis1" src="https://github.com/user-attachments/assets/4c3732a2-7190-466b-a9ed-ae3b56a0143e" />

<img width="1000" alt="hoteis2" src="https://github.com/user-attachments/assets/3071f4e2-a397-4d8b-9880-b8c0f24389fe" />

</details>

<details>
<summary><strong>❌ Cadastro de Hotel com Informações Inválidas</strong></summary>

<br>

- O usuário logado e autenticado deve **selecionar a aba Perfil** no canto inferior da página inicial.
- Deve selecionar a opção **Cadastrar Novo Hotel** na parte de Ações Administrativas.
- Na tela seguinte, deve preencher as informações do Hotel a ser cadastrado. Caso alguma informação obrigatória esteja faltando, o cadastro não é realizado.

**Evidências**:

<img width="400" alt="hoteis3" src="" />

<img width="1000" alt="hoteis4" src="" />

</details>

</details>

# Referências

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

