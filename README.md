# Projeto Prático - Microsserviços com Spring Boot e Spring Cloud

Este projeto foi desenvolvido durante o curso **"Microsserviços Java com Spring Boot e Spring Cloud" do instrutor Nelio Alves** utilizando **Java 11** e **Spring Boot 2.3.4**. 

**PS: DESENVOLVIMENTO EM ANDAMENTO**.

> **Observação:**  
> Este projeto utiliza versões e recursos considerados "antigos", mas serve como uma base de conhecimento valiosa para manutenção ou migração de projetos legados.

---

## Visão Geral do Projeto

O sistema é composto por diversos microsserviços que se comunicam de forma transparente e escalável. Em sua forma simplificada, o projeto possui os seguintes componentes principais:

- **Serviço de Trabalhadores (Worker):**  
  Responsável por gerenciar o cadastro de trabalhadores, estando conectado a um banco de dados para armazenamento de informações.

- **Serviço de Folha de Pagamento:**  
  Quando precisa de informações sobre um trabalhador, esse serviço realiza uma chamada para o microserviço de Trabalhadores utilizando apenas o nome do serviço. A infraestrutura, por meio de balanceamento de carga, escolhe uma das instâncias disponíveis e retorna a resposta de forma transparente.

- **API Gateway (Zuul):**  
  Atua como o ponto central de entrada para as requisições, roteando e autorizando o acesso aos diferentes microsserviços.

- **Servidor de Registro (Eureka):**  
  Responsável por registrar todos os microsserviços, permitindo que eles se descubram e comuniquem entre si.

Outros recursos e padrões importantes aplicados neste projeto incluem:

- **Feign:** Facilita as requisições de API entre os microsserviços.
- **Ribbon:** Implementa o balanceamento de carga entre as instâncias de um mesmo serviço.
- **Hystrix:** Garante tolerância a falhas, permitindo que o sistema continue operando mesmo se um dos serviços apresentar problemas.
- **OAuth e JWT:** Gerenciam a autenticação e autorização de forma segura.
- **Servidor de Configuração Centralizada:** Armazena as configurações dos microsserviços, integrando-se a um repositório Git.
- **Docker:** Gera containers para facilitar a implantação dos microsserviços e das bases de dados.

---

## Recursos do Projeto

- **Infraestrutura Completa de Microsserviços:**  
  Configuração automática, escalabilidade e balanceamento de carga.

- **Comunicação Transparente entre Serviços:**  
  Os microsserviços se comunicam via Eureka e são acessados pelo API Gateway.

- **Segurança:**  
  Implementação de autenticação e autorização utilizando OAuth e JWT.

- **Containerização:**  
  Preparação do ambiente para implantação com Docker.

---

## Tecnologias Utilizadas

- **Linguagem:** Java 11
- **Framework:** Spring Boot 2.3.4
- **Spring Cloud:** Conjunto de ferramentas para construção de microsserviços
- **Ferramentas e Bibliotecas:**  
  Feign, Ribbon, Hystrix, Eureka, Zuul, OAuth, JWT
- **Containerização:** Docker

---

## Como Executar o Projeto

1. **Pré-requisitos:**
    - Java 11 instalado
    - Docker (opcional, para containerização)
    - Git para clonagem do repositório

2. **Clonando o Repositório:**
   ```bash
   git clone <URL-do-Repositório>
