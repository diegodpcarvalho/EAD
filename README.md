# EAD AuthUser

Este é um projeto de gerenciamento de usuários para uma aplicação EAD, implementado com Spring Boot, utilizando Spring Data JPA para persistência de dados e HATEOAS para construção de links e navegação entre recursos. O projeto permite o cadastro, atualização e deleção de usuários, além de fornecer funcionalidades para login e gerenciamento de perfil.

## Tecnologias Utilizadas

- **Java 11** (ou superior)
- **Spring Boot 2.6.2**
- **Spring Data JPA**
- **Spring HATEOAS**
- **PostgreSQL** (banco de dados)
- **Maven** (gerenciamento de dependências)

## Funcionalidades

- Cadastro de usuários
- Atualização de informações de usuário (nome, telefone, etc.)
- Alteração de senha de usuário
- Gerenciamento de imagem de perfil de usuário
- Listagem de usuários com paginação
- Suporte a HATEOAS para links de navegação

## Como Rodar o Projeto

### 1. **Pré-requisitos**

Antes de rodar o projeto, você precisa ter o seguinte instalado:

- **Java 11** (ou superior)
- **Maven** (para gerenciamento de dependências e construção do projeto)
- **PostgreSQL** (ou outro banco de dados configurado no `application.properties`)

### 2. **Configuração do Banco de Dados**

Crie um banco de dados PostgreSQL e configure as credenciais no arquivo `src/main/resources/application.properties`:

```properties
spring.datasource.url=jdbc:postgresql://localhost:5432/nome_do_banco
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha
spring.jpa.hibernate.ddl-auto=update
spring.jpa.properties.hibernate.format_sql=true
3. Rodando a Aplicação
Para rodar o projeto localmente, execute o seguinte comando no terminal:
```
bash
Copiar código
mvn spring-boot:run
Isso irá iniciar a aplicação no servidor local (geralmente na URL http://localhost:8080).

4. Testando a API
Após a aplicação estar rodando, você pode acessar a API para testar as funcionalidades.

GET /users: Listar todos os usuários (com paginação)
GET /users/{userId}: Obter um usuário específico
POST /users: Criar um novo usuário
PUT /users/{userId}: Atualizar as informações de um usuário
DELETE /users/{userId}: Deletar um usuário
