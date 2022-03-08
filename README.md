# Human Resources

Este projeto foi desenvolvido no curso Full Stack Spring React da <a href="https://devsuperior.com.br/" target="_blank">DevSuperior</a> no módulo de Microservices, ele consiste no desenvolvimento de um sistema de cálculo do salário de trabalhadores com base na arquitetura de Microservices utilizando as tecnologias mais atuais no mercado, essa arquitetura torna o sistema altamente escalável, abaixo segue uma descrição resumida das tecnologias:

## **Tecnologias**

- Linguagem de programação: Java 11
- Framework: Spring Boot 2.3.x
- Banco de dados de teste H2
- Banco de dados de produção Postgresql 
- Ferramenta para testes de requisição Postman
- Docker para criação de containers e teste de produção

## **Descrição dos micreservices**

- Microservices
  - HR Api Gateway Zuul: microservice de roteamento, responsável pelo recebimento das requisições;
  - HR Config Server: microservice de configuração, responsável por acessar o repositório de configurações no Github;
  - HR Eureka Server: micorservice servidor, responsável por alocar os microservices clientes e fazer o balanceamento das requisições; 
  - HR Oauth: microservice de autenticação e autorização, responsável por liberar e validar os tokens dos clientes;
  - HR User: microservice da entidade usuário, responsável por acessar os usuários no base de dados;
  - HR Worker: microservice da entidade trabalhadores, responsável por acessar os trabalhadores na base de dados;
  - HR Payroll: microserice da folha de pagamento, responsável por fazer o cálculo do salário dos trabalhadores;

## **Implementações do framework**

- Actuator;
- Eureka;
- Feign Client;
- Rest Template;
- Ribbon Load Balancing;
- Zuul API Gateway;

## Imagens o projeto

adicionar...

## Executando o projeto

Baixe o código fonte e o extraia em seu diretório de preferência, exemplo (C:\Workspaces).

Abra as pastas dos microservices com a sua IDE Java de preferência, recomendação (Spring Tools ou VS Code), aguarde o Maven baixar as dependências e depois execute os microservices seguindo os passos abaixo:

 1. HR Config Server: para puxar as configurações do Github
 2. HR Eureka Server: para alocar os clientes
 3. O restanto dos micreservices podem ser iniciados na ordem de sua preferência
 4. Aguarde de 3 a 5 minutos para que os clientes estabilizem no servidor e após isso pode iniciar os testes

### Usuários para teste

Usuário 1: nina@gmail.com, senha: 123456

Usuário 2: leia@gmail.com, senha: 123456

