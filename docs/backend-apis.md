# APIs e Web Services

O sistema distribuído visa proporcionar uma plataforma de gestão hoteleira, agregando vários módulos independentes para suprir as necessidades básicas dos usuários, administração e o próprio hotel. A ferramenta oferece funcionalidades essenciais como autenticação segura, cadastro e validação de usuários, gerenciamento de hotéis e quartos, realização e controle de reservas, avaliações de estadia e integração com meios de pagamento.

Cada módulo foi projetado para operar de forma autônoma e comunicável via Web APIs, garantindo flexibilidade, escalabilidade e fácil manutenção do sistema. Toda a comunicação entre os módulos ocorre por meio de requisições HTTP e respostas em JSON, assegurando interoperabilidade, segurança e flexibilidade.

## Objetivos da API

O principal objetivo da API é centralizar e padronizar a comunicação entre os diferentes módulos do sistema distribuído, garantindo integração segura, eficiente e escalável entre os serviços. A API foi projetada para permitir tanto o uso interno (entre os módulos do próprio sistema) quanto o uso externo controlado (por aplicações clientes, como um painel administrativo ou aplicativo móvel).

Os objetivos específicos da API incluem:

1. **Gerenciar o ciclo de vida das reservas:**  
   Permitir que usuários autenticados possam criar, listar, atualizar e excluir reservas de quartos de forma simples e segura, mantendo o vínculo entre reserva, usuário e quarto.

2. **Centralizar autenticação e controle de acesso:**  
   Oferecer endpoints para cadastro, login e autenticação via JWT, garantindo que apenas usuários autorizados acessem os recursos apropriados.

3. **Padronizar a comunicação entre serviços:**  
   Servir como camada intermediária entre os módulos de usuários, quartos e reservas, utilizando o formato JSON e o protocolo HTTP com métodos RESTful.

4. **Garantir segurança e rastreabilidade:**  
   Aplicar políticas de autenticação, autorização e registro de ações (logs) para assegurar integridade e confiabilidade dos dados.

5. **Promover escalabilidade e modularidade:**  
   Manter os serviços desacoplados, permitindo que cada módulo evolua de forma independente e possa ser escalado conforme a demanda.

## Modelagem da Aplicação

[Descreva a modelagem da aplicação, incluindo a estrutura de dados, diagramas de classes ou entidades, e outras representações visuais relevantes.]

## Tecnologias Utilizadas

### Backend
- **FastAPI:** Framework principal para criação da API RESTful.  
- **Python 3.13:** Linguagem de programação utilizada no backend.

### Banco de Dados
- **PostgreSQL:** Sistema gerenciador de banco de dados relacional (SGBD) utilizado para armazenamento das informações.  
- **SQLAlchemy:** ORM responsável por fazer a ponte entre o banco de dados e as entidades Python.

### Autenticação e Segurança
- **JWT (JSON Web Token):** Utilizado para autenticação e controle de acesso dos usuários.  
- **Passlib / bcrypt:** Bibliotecas utilizadas para criptografar senhas com segurança antes de armazená-las no banco de dados.

### Arquitetura e Organização
- **Pydantic:** Usado para definir e validar schemas de entrada e saída, garantindo consistência nos dados trafegados pela API.  
- **Uvicorn:** Servidor ASGI de alta performance responsável por executar a aplicação FastAPI, oferecendo suporte a requisições assíncronas e escalabilidade horizontal.

### Ambiente e Execução
- **Virtualenv (.venv):** Isolamento do ambiente Python para controle de dependências.  
- **Git e GitHub:** Controle de versão e colaboração entre desenvolvedores.

## API Endpoints

### Endpoint Reservas

- **Método:** GET  
- **URL:** /reservas  
- **Resposta:**  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "id": "081274f3-9feb-45a2-8296-c9205ff56af0",
            "user_id": "123",
            "room_id": 222,
            "date_checkin": "2025-12-20T14:00:00",
            "date_checkout": "2025-12-30T12:00:00"
        }
    }
    ```
  - Sucesso (200 OK, sem reservas)
    ```json
    {
        "message": "Success",
        "data": []
    }
    ```

- **Método:** GET  
- **URL:** /reservas/{id_reserva}  
- **Resposta:**  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "id": "081274f3-9feb-45a2-8296-c9205ff56af00",
            "user_id": "123",
            "room_id": 222,
            "date_checkin": "2025-12-20T14:00:00",
            "date_checkout": "2025-12-30T12:00:00"
        }
    }
    ```
  - Erro (404 Not Found)
    ```json
    {
        "message": "Erro",
        "data": {
            "detail": "Reservation not found"
        }
    }
    ```

- **Método:** POST  
- **URL:** /reservas  
- **Parâmetros:**  
    ```json
    {
        "room_id": 222,
        "date_checkin": "2025-12-20T14:00:00",
        "date_checkout": "2025-12-30T12:00:00"
    }
    ```
- **Resposta:**  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "id": "081274f3-9feb-45a2-8296-c9205ff56af0",
            "user_id": "123",
            "room_id": 222,
            "date_checkin": "2025-12-20T14:00:00",
            "date_checkout": "2025-12-30T12:00:00"
        }
    }
    ```

- **Método:** PATCH  
- **URL:** /reservas/{id_reserva}  
- **Resposta:**  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "id": "081274f3-9feb-45a2-8296-c9205ff56af0",
            "user_id": "123",
            "room_id": 999,
            "date_checkin": "2025-12-22T14:00:00",
            "date_checkout": "2025-12-28T12:00:00"
        }
    }
    ```
  - Erro (404 Not Found)
    ```json
    {
        "message": "Erro",
        "data": {
            "detail": "Reservation not found"
        }
    }
    ```

- **Método:** DELETE  
- **URL:** /reservas/{id_reserva}  
- **Resposta:**  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "message": "Reservation 081274f3-9feb-45a2-8296-c9205ff56af0 deleted successfully"
        }
    }
    ```
  - Erro (404 Not Found)
    ```json
    {
        "message": "Erro",
        "data": {
            "detail": "Reservation not found"
        }
    }
    ```

### Endpoint Avaliações

- **Método:** GET  
- **URL:** /hotels/{hotel_id}/reviews  
- **Parâmetros:** hotel_id: O ID do hotel que você deseja consultar.

**Respostas:**  
- Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": [
            {
                "rating": 5,
                "comment": "Excelente estadia!",
                "id": 1,
                "hotel_id": 1,
                "user": {
                    "user_name": "john_doe"
                }
            }
        ]
    }
    ```
- Erro (404 Not Found)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Hotel not found"
        }
    }
    ```

- **Método:** POST  
- **URL:** /hotels/{hotel_id}/reviews  
- **Parâmetros:** Request Body JSON
    ```json
    {
        "rating": 5,
        "comment": "Adorei a experiência!"
    }
    ```
- Respostas:  
  - Sucesso (201 Created)
    ```json
    {
        "message": "Success",
        "data": {
            "rating": 5,
            "comment": "Adorei a experiência!",
            "id": 2,
            "hotel_id": 1,
            "user": {
                "user_name": "john_doe"
            }
        }
    }
    ```
  - Erro (401 Unauthorized)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Não há um usuário 'logado'. Por favor, faça o login."
        }
    }
    ```

- **Método:** PUT  
- **URL:** /reviews/{review_id}  
- **Parâmetros:** Request Body JSON
    ```json
    {
        "rating": 3,
        "comment": "Atualizando meu comentário."
    }
    ```
- Respostas:  
  - Sucesso (200 OK)
    ```json
    {
        "message": "Success",
        "data": {
            "rating": 3,
            "comment": "Atualizando meu comentário.",
            "id": 2,
            "hotel_id": 1,
            "user": {
                "user_name": "john_doe"
            }
        }
    }
    ```
  - Erro (403 Forbidden)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Not authorized"
        }
    }
    ```
  - Erro (404 Not Found)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Review not found"
        }
    }
    ```

- **Método:** DELETE  
- **URL:** /reviews/{review_id}  
- **Respostas:**  
  - Sucesso (204 No Content)  
    *Sem corpo de resposta*  
  - Erro (403 Forbidden)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Not authorized"
        }
    }
    ```
  - Erro (404 Not Found)
    ```json
    {
        "message": "Error",
        "data": {
            "detail": "Review not found"
        }
    }
    ```

## Considerações de Segurança

[Discuta as considerações de segurança relevantes para a aplicação distribuída, como autenticação, autorização, proteção contra ataques, etc.]

## Implantação

1. Defina os requisitos de hardware e software necessários para implantar a aplicação em um ambiente de produção.  
2. Escolha uma plataforma de hospedagem adequada, como um provedor de nuvem ou um servidor dedicado.  
3. Configure o ambiente de implantação, incluindo a instalação de dependências e configuração de variáveis de ambiente.  
4. Faça o deploy da aplicação no ambiente escolhido.  
5. Realize testes para garantir que a aplicação esteja funcionando corretamente no ambiente de produção.

## Testes

- [**Testes Users**](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2025-2-pe6-t3-g3-t3-2025-2/blob/main/docs/users-api-testing.md)  
- [**Testes Auth**](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2025-2-pe6-t3-g3-t3-2025-2/blob/main/docs/auth-api-testing.md)  
- [**Testes Reservas**](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2025-2-pe6-t3-g3-t3-2025-2/blob/main/docs/reservas-api-testing.md)
- [**Testes hotéis**](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2025-2-pe6-t3-g3-t3-2025-2/blob/main/docs/hotels-api-testing.md)
- [**Testes comodidades dos hotéis**](https://github.com/ICEI-PUC-Minas-PMV-SI/pmv-si-2025-2-pe6-t3-g3-t3-2025-2/blob/main/docs/amenities-api-testing.md)

# Referências

~~Inclua todas as referências (livros, artigos, sites, etc) utilizados no desenvolvimento do trabalho.~~
1. **Documentação FASTAPI**: https://fastapi.tiangolo.com/#typer-the-fastapi-of-clis
2. **Documentação Python 3.13**: https://docs.python.org/pt-br/3/
3. **Documentação PostgreeSQL**: https://www.postgresql.org/docs/current/index.html
4. **Documentação Uvicorn**: https://uvicorn.dev/

# Planejamento

## Quadro de tarefas

### Semanas 1-5

Atualizado em: 05/10/2025

| Responsável | Tarefa/Requisito      | Iniciado em | Prazo      | Status | Terminado em |
|------------|----------------------|------------|-----------|--------|--------------|
| Victor Pereira, Gustavo Rossetti, Luiz Andrade, Matheus Fraga     | Documentação          | 01/09/2025 | 05/10/2025 | ⌛     | 05/10/2025   |
| Victor Pereira     | Desenvolvimento da API (feature de Reservas de Hospedagens)          | 01/09/2025 | 28/09/2025 | ✔️     | 05/10/2025   |
| Matheus Fraga     | Desenvolvimento da API (feature de Hotéis)          | 01/09/2025 | 28/09/2025 | ✔️     | 05/10/2025   |
| Luiz Andrade     | Desenvolvimento da API (feature de Usuários/Login/Autenticação)          | 01/09/2025 | 28/09/2025 | ✔️     | 05/10/2025   |
| Gustavo Rossetti     | Desenvolvimento da API (feature de Comodidades dos Hotéis)          | 01/09/2025 | 28/09/2025 | ✔️     | 05/10/2025   |
| Victor Pereira     | Testes da API (feature de Reservas de Hospedagens)          | 28/09/2025 | 05/10/2025 | ✔️     | 05/10/2025   |
| Matheus Fraga     | Testes da API (feature de Hotéis)          | 28/09/2025 | 05/10/2025 | ✔️     | 05/10/2025   |
| Luiz Andrade     | Testes da API (feature de Usuários/Login/Autenticação)          | 28/09/2025 | 05/10/2025 | ✔️     | 05/10/2025   |
| Gustavo Rossetti     | Testes da API (feature de Comodidades dos Hotéis)          | 28/09/2025 | 05/10/2025 | ✔️     | 05/10/2025   |

Legenda:  
✔️: terminado  
📝: em execução  
⌛: atrasado  
❌: não iniciado
