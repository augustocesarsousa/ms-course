# Human Resources

Este projeto foi desenvolvido no curso Full Stack Spring React da <a href="https://devsuperior.com.br/" target="_blank">DevSuperior</a> no módulo de Microservices, ele consiste no desenvolvimento de um sistema de cálculo do salário de trabalhadores, utilizando a arquitetura de Microservices, essa arquitetura torna o sistema altamente escalável de fácil manutenção e disponibilidade, abaixo segue uma descrição resumida das tecnologias implementadas:

## **Tecnologias**

- Linguagem de programação: Java 11
- Framework: Spring Boot 2.3.x
- Banco de dados de teste H2
- Banco de dados de produção Postgresql
- Ferramenta para testes de requisição Postman
- Docker para criação de containers e teste de produção

## **Descrição dos microservices**

- Hr Api Gateway Zuul: microservice de roteamento, responsável pelo recebimento das requisições
- Hr Config Server: microservice de configuração, responsável por acessar o repositório de configurações no Github
- Hr Eureka Server: micorservice servidor, responsável por alocar os microservices clientes e fazer o balanceamento das requisições
- Hr Oauth: microservice de autenticação e autorização, responsável por liberar e validar os tokens dos clientes
- Hr User: microservice da entidade usuário, responsável por acessar os usuários no base de dados
- Hr Worker: microservice da entidade trabalhadores, responsável por acessar os trabalhadores na base de dados
- Hr Payroll: microservice da folha de pagamento, responsável por fazer o cálculo do salário dos trabalhadores

## **Implementações do framework**

- Actuator
- Eureka
- Feign Client
- Rest Template
- Ribbon Load Balancing
- Zuul API Gateway

## Imagens o projeto

1. Listagem dos microservices

![microservices list](/images/microservices.png)

2. Executando microservices em containers Docker

![containers](/images/containers_docker.png)

3. Eureka server (listagem dos microservices em execução)

![eureka server](/images/eureka.png)

4. Endpoint autenticação e liberação do token para acesso aos endpoints privados

![endpoit login](/images/endpoint_login.png)

5. Endpoint user by email

![endpoit user by email](/images/endpoint_user_by_email.png)

6. Endpoint worker by id

![endpoit worker by id](/images/endpoint_worker_by_id.png)

7. Endpoint payment (cálculo do salário)

![endpoit payment](/images/endpoint_payment.png)

## Executando o projeto

Baixe o código fonte e o extraia em seu diretório de preferência, exemplo (C:\Workspaces).

Importe os microservices com a sua IDE Java de preferência, recomendação (Spring Tools ou VS Code), aguarde o Maven baixar as dependências e depois execute os microservices seguindo os passos abaixo:

1.  HR Config Server: para puxar as configurações do Github
2.  HR Eureka Server: para alocar os clientes
3.  O restante dos microservices podem ser iniciados na ordem de sua preferência
4.  Aguarde de 3 a 5 minutos para que os clientes estabilizem no servidor e após isso pode iniciar os testes

### Usuários para teste

Usuário 1: nina@gmail.com, senha: 123456

Usuário 2: leia@gmail.com, senha: 123456
