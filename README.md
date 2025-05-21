# javaSpringBootErudio2025

Projeto realizado para acompanhar o curso da udemy "Aprenda Spring Boot framework Swagger Docker Kubernetes K8s API RESTful
JWT JUnit 5 Mockito React JS do 0 à AWS e GCP e+" e aprender seus conceitos.

# Person

Este projeto implementa serviços HTTP (`POST`, `GET`, `DELETE` e `PUT`) utilizando Java com Spring Boot. Inicialmente, os dados eram simulados com [mocks](#o-que-é-um-mock), mas o projeto foi evoluído para realizar operações reais de CRUD utilizando um banco de dados MySQL com JPA (Java Persistence API).

## FindByID

Retorna uma pessoa de acordo com o seu ID:

<br>

![Exemplo FindByID](imgs/06-findById.png)

## FindAll

Retorna todas as pessoas presentes no [mock](#o-que-é-um-mock):

<br>

![Exemplo FindAll](imgs/06-findAll.png)

## Create

Cria uma pessoa:

<br>

![Exemplo Create](imgs/06-create.png)

## Update

Atualiza os dados de uma pessoa:

<br>

![Exemplo Update](imgs/06-update.png)

## Delete

Deleta os dados de uma pessoa:

<br>

![Exemplo Delete](imgs/06-Delete.png)

## Logs no Spring Boot

O projeto também utiliza logs para registrar o comportamento da aplicação durante a execução, facilitando o processo de depuração e monitoramento.

Para isso, foi utilizada a biblioteca **SLF4J** (Simple Logging Facade for Java), que fornece uma interface para diversas implementações de logging.

### Níveis de log disponíveis:

- `TRACE` – nível mais detalhado, geralmente usado para rastreamento fino
- `DEBUG` – informações úteis para desenvolvedores durante a depuração
- `INFO` – mensagens informativas sobre o fluxo normal da aplicação
- `WARN` – indica situações de alerta que não interrompem o sistema
- `ERROR` – indica falhas ou erros que exigem atenção

> Os logs ajudam a manter o controle do que está acontecendo na aplicação sem a necessidade de usar `System.out.println()`.

## Padrão DTO com Dozer Mapper

O projeto também adota o padrão **DTO (Data Transfer Object)** para separar a camada de apresentação dos modelos de entidade. Isso promove maior segurança, controle e clareza na exposição de dados via API.

Para realizar a conversão entre entidades e DTOs, foi utilizada a biblioteca **Dozer Mapper**, que simplifica o mapeamento automático entre objetos com estruturas semelhantes.

### Vantagens do uso de DTOs:

- Evita exposição direta de entidades JPA

- Facilita a criação de respostas customizadas

- Permite maior controle sobre os dados trafegados na API

- Ajuda na validação de entrada e saída de dados

> 📌 À medida que novos endpoints forem adicionados, novos DTOs serão criados para representar os dados da forma mais adequada para cada caso de uso.

## O que é um Mock?

Um _mock_ é uma simulação de um objeto real. Em contextos de desenvolvimento e testes, mocks são usados para representar dados ou comportamentos esperados de componentes que ainda não foram implementados, ou que não se deseja acessar diretamente (como chamadas a APIs externas ou bancos de dados).

No contexto deste projeto, o _mock_ de pessoa é uma classe ou objeto com atributos pré-definidos (como nome, idade, CPF, etc.) que representa uma instância de `Person`. Ele é utilizado para simular uma requisição HTTP de criação de pessoa, facilitando o desenvolvimento e os testes do serviço sem depender de entradas externas.

## Spring Boot Initializr

Para gerar um novo projeto Spring Boot, acesse o [Spring Initializr](https://start.spring.io/).

### Dependências utilizadas:

[pom.xml](https://github.com/BredexBR/javaSpringBootErudio2025/blob/main/javaSpringBootErudio2025/pom.xml)

## Pré-requisitos

1. **Java 21**: Certifique-se de que o Java 21 está instalado na sua máquina.
2. **Docker**: Necessário para a execução de containers. Versão 27.4.0.
3. **MySQL**: Configuração do banco de dados. Versão 8.0.40.
4. **Postman**: Para testar a API.
5. **Java Spring Tool**: Framework na versão 3.3.7.
6. **Mvn**: Gerenciar as dependências e automatizar as builds. Versão 3.3.9.
