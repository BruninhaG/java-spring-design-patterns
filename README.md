# 🏆 Desafio de Projeto: Design Patterns com Java e Spring

### 🚀 **Foco:** Aplicação de Padrões de Projeto (GoF) no contexto de uma API RESTful.

Este repositório contém a reprodução e aprimoramento do projeto laboratorial sobre **Design Patterns com Java**, realizado pela **Digital Innovation One (DIO)**.

O projeto consiste em uma API Spring Boot para **Gerenciamento de Clientes**, que demonstra o uso de diferentes padrões de projeto, clássicos (GoF) e do Spring Framework, no contexto da integração com a **API ViaCep** para consulta automática de endereços.

---

## 🏗️ Design Patterns Aplicados (O Coração do Projeto)

Esta aplicação foi estruturada usando princípios de *Clean Code* e Design Orientado a Objetos. Os principais Padrões de Projeto aplicados são:

| Categoria | Padrão de Projeto | Aplicação no Projeto |
| :--- | :--- | :--- |
| **GoF - Estrutural** | **Facade** | O serviço de cliente (`ClienteService`) atua como uma **Facade**, simplificando a interface para o subsistema que envolve a manipulação de clientes e a busca de CEPs (ViaCep Service). |
| **GoF - Comportamental** | **Strategy** | *(Sugestão: Descreva aqui um padrão comportamental, ex: Para diferentes regras de validação.)* |
| **Spring/GoF - Criação** | **Singleton** | Todos os componentes do Spring (Service, Repository, Controller) são gerenciados como **Singletons** no Contexto IoC. |
| **Spring Framework** | **Dependency Injection (DI)** | A aplicação utiliza o padrão Inversão de Controle (IoC) para gerenciar as dependências entre os componentes. |

***Nota:** Personalize a tabela acima com os padrões específicos que você implementou de fato no seu código.*

---

## 🎯 Visão Geral da Funcionalidade

Esta aplicação é uma API RESTful completa para gerenciamento de clientes, que utiliza o cliente **Feign** para se comunicar com a API ViaCep.

### 🧩 Funcionalidades

A API expõe operações CRUD (Create, Read, Update, Delete) sobre o recurso `Cliente`:

* Recuperar todos os clientes e seus detalhes.
* Consultar um único cliente pelo ID.
* Adicionar novos clientes, **buscando e preenchendo automaticamente os dados do endereço** via ViaCep.
* Atualizar informações de clientes existentes.
* Excluir clientes do sistema.

### 🔗 Endpoints RESTful

| Método | Endpoint | Descrição |
| :--- | :--- | :--- |
| `GET` | `/clientes` | Busca e lista todos os clientes cadastrados. |
| `GET` | `/clientes/{id}` | Recupera os detalhes de um cliente específico pelo seu ID. |
| `POST` | `/clientes` | Adiciona um novo cliente, incluindo o endereço do CEP informado. |
| `PUT` | `/clientes/{id}` | Atualiza os detalhes de um cliente existente. |
| `DELETE` | `/clientes/{id}` | Remove um cliente do sistema. |

---

## ⚙️ Como Executar o Projeto

Siga estas etapas para clonar e rodar a aplicação Spring Boot localmente:

### 1. Pré-requisitos

Certifique-se de ter as seguintes ferramentas instaladas:

* **Java Development Kit (JDK)**: Versão 17 ou superior.
* **Maven** (ou Gradle): Para gerenciar as dependências e o *build* do projeto.
* **Git**: Para clonar o repositório.

### 2. Clonar o Repositório

Abra seu terminal ou prompt de comando e execute:

```bash
git clone [https://github.com/BruninhaG/java-spring-design-patterns]
cd java-spring-design-patterns
 ```

### 3. Construção e Execução (Maven)

Execute os comandos a seguir para compilar e iniciar o aplicativo Spring Boot:

**Compilar e instalar as dependências:**
```bash
mvn clean install
```

**Executar a aplicação:**
```bash
mvn spring-boot:run
```

### 4. Acessar a Aplicação
A aplicação estará rodando em http://localhost:8080. Você pode testar os endpoints usando ferramentas como Postman ou cURL.
- Exemplo de Acesso: GET http://localhost:8080/clientes

---

##  🌐 API Externa Utilizada
A aplicação faz uso da API ViaCep para consultas de endereços baseadas em códigos postais (CEPs):
- ViaCep API

---

## 🛠️ Tecnologias Utilizadas
- **Linguagem**: Java
- **Framework**: Spring Boot
- **Acesso a Dados**: Spring Data JPA
- **Client HTTP**: Spring Cloud OpenFeign
- **Build Tool**: Maven (ou Gradle)

---

## 👩‍💻 Autora
Feito com 💛 por Bruna Guimarães

## 🌟 Apoie o projeto
Se você gostou, não esqueça de deixar uma ⭐ no repositório!
Isso ajuda muito o projeto a crescer e me incentiva a continuar criando. 🙌
