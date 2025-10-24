# 🚀 Desafio de Projeto — Microsserviços com Spring Boot

Este projeto foi desenvolvido como parte de um **Desafio de Projeto da DIO (Digital Innovation One)**.  
O objetivo é construir uma **arquitetura de microsserviços em Java**, aplicando conceitos modernos de comunicação síncrona e assíncrona utilizando **Spring Boot** e **RabbitMQ**.

---

## 🧩 Descrição do Desafio

O desafio consiste na criação de dois microsserviços independentes e integrados:

- **Warehouse (Armazém)** — responsável pela gestão de produtos e controle de estoque.  
- **Storefront (Vitrine)** — responsável por simular a experiência do cliente e consumir os dados do armazém.

Os microsserviços se comunicam:
- De forma **síncrona**, por meio de **requisições HTTP REST**;
- E de forma **assíncrona**, via mensageria utilizando **RabbitMQ** hospedado no **CloudAMQP**.

---

## 🎯 Objetivos de Aprendizagem

Ao finalizar este desafio, você será capaz de:

- Estruturar um projeto de microsserviços em **Spring Boot**;
- Configurar comunicação **síncrona e assíncrona** entre aplicações;
- Utilizar o **RabbitMQ** com o serviço de nuvem **CloudAMQP**;
- Aplicar conceitos de arquitetura limpa, isolamento e escalabilidade;
- Documentar e versionar o projeto profissionalmente no **GitHub**.

---

## ⚙️ Tecnologias e Ferramentas

| Tecnologia | Versão / Descrição |
|-------------|--------------------|
| **Java** | 21 |
| **Spring Boot** | 3.5.6 |
| **Lombok** | Redução de boilerplate de código |
| **Spring Data JPA** | Persistência de dados |
| **H2 Database** | Banco de dados em memória para testes |
| **Spring Web** | Criação de APIs REST |
| **Spring for RabbitMQ** | Mensageria e comunicação assíncrona |
| **Spring Boot DevTools** | Hot reload durante o desenvolvimento |
| **Gradle (Kotlin DSL)** | Gerenciador de dependências |
| **CloudAMQP** | RabbitMQ hospedado em nuvem |

---

## 🏗️ Estrutura dos Microsserviços

microsservicos/
├── warehouse/ # Microsserviço de controle de produtos e estoque
│ ├── src/
│ ├── build.gradle.kts
│ └── application.yml
│
└── storefront/ # Microsserviço de vitrine e consumo de dados do armazém
├── src/
├── build.gradle.kts
└── application.yml


Cada microsserviço possui sua própria configuração e base de dados, permitindo deploy e escalabilidade independentes.

---

## 🔗 Comunicação Entre os Serviços

| Tipo de Comunicação | Tecnologia | Descrição |
|---------------------|-------------|------------|
| **Síncrona** | REST / HTTP | Comunicação direta entre os microsserviços via API |
| **Assíncrona** | RabbitMQ / CloudAMQP | Troca de mensagens de eventos, como atualização de estoque e compras |

---

## ☁️ Integração com CloudAMQP

Para a comunicação assíncrona foi utilizada uma instância gratuita do **CloudAMQP**, com o **RabbitMQ** configurado como broker.

**Exemplo genérico de configuração (`application.yml`):**

```yaml
spring:
  rabbitmq:
    host: your-cloudamqp-host
    port: 5672
    username: your-username
    password: your-password

🚀 Como Executar o Projeto
🔧 Pré-requisitos

JDK 21+

Gradle 8+

Conta no CloudAMQP

IDE - (IntelliJ, Eclipse ou VS Code)

📚 Aprendizados e Boas Práticas

Durante o desenvolvimento deste projeto foram aplicados princípios de:

Arquitetura de microsserviços e isolamento de contexto;

Comunicação via APIs REST e mensageria assíncrona;

Utilização de ferramentas modernas do ecossistema Spring Boot;

Padronização de versionamento e documentação no GitHub.
