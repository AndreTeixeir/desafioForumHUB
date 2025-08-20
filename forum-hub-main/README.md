<p align="center">
<img src = "ONE_logo_rgb.png" width="300" height="150">
</p>
  <p align="center">
   <img src="https://img.shields.io/badge/Framework-Spring-blue"> <img src="https://img.shields.io/badge/Language-Java%2021.07-orange"> <img src="https://img.shields.io/badge/Database-MySQL-green"> 
  </p>

<a id="readme-top"></a>
# 📚 Forum Hub

O **Forum Hub** é uma API RESTful construída com Spring Boot para gerenciamento de um fórum de discussão. A aplicação permite o cadastro, detalhamento, atualização e exclusão de tópicos, autenticação de usuários com JWT, promovendo uma estrutura robusta e segura para aplicações web modernas.

---

## 🚀 Funcionalidades principais:

- ✅ Cadastro e autenticação de usuários com JWT
- ✅ Registro, detalhamento, atualização e exclusão de tópicos
- ✅ Listagem paginada de tópicos com filtros
- ✅ Validação de regras de negócio
- ✅ Controle de acesso baseado em perfil (ex: ADMIN)
- ✅ Tratamento de exceções e respostas padronizadas

---

## 🛠️ Tecnologias e frameworks utilizados:

- **Java 17**
- **Spring Boot 3**
- **Spring Security** (com JWT)
- **Spring Data JPA**
- **Hibernate**
- **MySQL**
- **Flyway** (para versionamento de banco de dados)
- **Lombok**
- **JPA Specification / JPQL**
- **Bean Validation**
- **OpenAPI/Swagger** (para documentação)

---

## ✅ Requisitos para executar a aplicação:

- [JDK 17+](https://www.oracle.com/java/technologies/javase/jdk17-archive-downloads.html)
- [Maven 3.8+](https://maven.apache.org/install.html)
- [MySQL Server](https://dev.mysql.com/downloads/mysql/) (ou banco equivalente configurado no `application.properties`)
- [Insomnia](https://insomnia.rest/) ou outro HTTP Client (opcional, para testes)

---

## 🎯 Configuração do Banco de Dados:

Antes de rodar a aplicação, configure o arquivo:

```
src/main/resources/application.properties
```

Exemplo:

```properties
spring.datasource.url=jdbc:mysql://localhost:8080/forum
spring.datasource.username=seu_usuario
spring.datasource.password=sua_senha

spring.jpa.hibernate.ddl-auto=update
spring.jpa.show-sql=true
spring.jpa.properties.hibernate.format_sql=true
```

> Obs: Certifique-se de ter criado um banco de dados chamado `forum` no MySQL.

---

## 🔐 Configuração de Secret do Token JWT

No arquivo:
```
src/main/resources/application.properties
```

Exemplo:

```properties
api.security.token.secret=${SUA_SENHA}
```
> Obs: Recomendo o uso de variáveis de ambiente para todas as configurações do arquivo.
___

## 📦 Como rodar a aplicação:

### 1. Clone o repositório

```bash
git clone https://github.com/AndreTeixeir/forum-hub.git
cd forum-hub
```

### 2. Crie o banco de dados

No MySQL, crie um banco com o nome:

```sql
CREATE DATABASE forum;
```

> Caso esteja usando Flyway, ele criará as tabelas automaticamente.

### 3. Configure o arquivo `application.properties`

Preencha com seus dados de conexão (usuário/senha do banco).

### 4. Rode a aplicação com Maven

```bash
./mvnw spring-boot:run
```

### 5. Teste os endpoints

Você pode usar o Postman, Insomnia ou até mesmo o Swagger, se estiver habilitado. Os principais endpoints são:

- `POST /login` → Autenticação
- `GET /topicos` → Listagem de tópicos
- `GET /topicos/${id}` → Detalha o tópico selecionado pelo ID
- `POST /topicos` → Criação de novo tópico
- `DELETE /topicos/{id}` → Exclusão do tópico
- `DELETE /resolved/{id}` → Altera o status do tópico para resolvido. O tópico não aparecerá no método de listagem, mas não será excluído do banco. 

---

## 👩‍💻 Desenvolvedor:

  André Teixeira

**[LinkedIn](https://www.linkedin.com/in/andré-teixeira-15503046/)** | **[GitHub](https://github.com/AndreTeixeir)**

_Este projeto faz parte do desafio **ForumHub** do programa **Oracle Next Generation (ONE) em parceria com a Alura**._

_____________________________
