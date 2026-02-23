# Aprendendo Spring - API de Gerenciamento de Usuários

Este projeto é uma API REST desenvolvida com **Spring Boot** para o gerenciamento de usuários, incluindo funcionalidades de autenticação segura via **JWT (JSON Web Tokens)** e integração com banco de dados **PostgreSQL**.

## 🚀 Funcionalidades

- **CRUD de Usuários**: Cadastro, consulta e exclusão de usuários com seus respectivos endereços e telefones.
- **Autenticação JWT**: Sistema de login seguro que gera tokens de acesso para proteger endpoints.
- **Segurança de Dados**: Implementação de criptografia de senhas utilizando o algoritmo BCrypt.
- **Tratamento de Exceções**: Retornos claros em caso de e-mails duplicados ou recursos não encontrados.

## 🛠️ Tecnologias Utilizadas

- **Java 17**
- **Spring Boot 4.x** (Starters: Web, Data JPA, Security)
- **PostgreSQL**: Banco de dados relacional.
- **JSON Web Token (JJWT)**: Para autenticação e autorização.
- **Lombok**: Para redução de código boilerplate.
- **Maven**: Gerenciador de dependências.

## 📁 Estrutura do Projeto

O projeto segue uma arquitetura organizada em camadas:
- `controller`: Endpoints da API.
- `business`: Lógica de negócio e serviços.
- `infrastructure`: Configurações técnicas, entidades, repositórios e segurança (JWT).

## ⚙️ Configuração e Execução

### Pré-requisitos
- JDK 17+
- PostgreSQL rodando localmente.

### Configuração do Banco de Dados
No arquivo `src/main/resources/application.properties`, configure as credenciais do seu PostgreSQL:
```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/db_usuario
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
```

### Executando a aplicação
```bash
./mvnw spring-boot:run
```

## 🔌 Endpoints de Exemplo

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `POST` | `/usuario` | Cria um novo usuário. |
| `POST` | `/usuario/login` | Realiza login e recebe o Token JWT. |
| `GET` | `/usuario?email={email}` | Busca dados do usuário por e-mail. |
| `DELETE` | `/usuario/{email}` | Remove um usuário por e-mail. |

---
*Desenvolvido como parte dos estudos de Spring Boot e Segurança.*
