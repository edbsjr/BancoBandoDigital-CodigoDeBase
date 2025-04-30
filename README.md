# 📌 Banco Digital

Este projeto é uma **API REST** de um banco digital, desenvolvido em **Java**.  
O objetivo é aplicar conceitos de orientação a objetos, frameworks e persistência de dados.

---

## 🚀 Funcionalidades

- ✅ Cadastro e gerenciamento de clientes  
- ✅ Criação de contas - corrente e poupança  
- ✅ Emissão de cartões - crédito e débito  
- ✅ Realização de pagamentos e simulação de saldo  
- ✅ Tratamento de exceções  
- ✅ Arquitetura baseada em camadas (Controller, Service, Repository, etc.)

---

## 🛠️ Tecnologias

- Java  
- Spring Boot  
- Spring Data JPA  
- H2 Database  
- Postman

---

## 📂 Estrutura do Projeto

- `src/controller` — Endpoints da API  
- `src/dto` — Objetos de transferência de dados (DTOs)  
- `src/entity` — Entidades JPA que representam as tabelas do banco  
- `src/repository` — Interfaces para acesso ao banco com Spring Data JPA  
- `src/service` — Regras de negócio e lógica da aplicação  
- `src/enums` — Enums utilizados no projeto  

Outros arquivos importantes:
- `README.md` — Documentação do projeto  
- `pom.xml` — Arquivo de build com as dependências do Maven



## 📡 Endpoints da API Banco Digital

### 🧍 Cliente

- `POST /clientes` — Criar um novo cliente  
- `GET /clientes/{id}` — Obter detalhes de um cliente  
- `PUT /clientes/{id}` — Atualizar informações de um cliente  
- `DELETE /clientes/{id}` — Remover um cliente  
- `GET /clientes` — Listar todos os clientes

### 💳 Conta

- `POST /contas` — Criar uma nova conta  
- `GET /contas/{id}` — Obter detalhes de uma conta  
- `POST /contas/{id}/transferencia` — Realizar uma transferência entre contas  
- `GET /contas/{id}/saldo` — Consultar saldo da conta  
- `POST /contas/{id}/pix` — Realizar um pagamento via Pix  
- `POST /contas/{id}/deposito` — Realizar um depósito na conta  
- `POST /contas/{id}/saque` — Realizar um saque da conta  
- `PUT /contas/{id}/manutencao` — Aplicar taxa de manutenção mensal (para conta corrente)  
- `PUT /contas/{id}/rendimentos` — Aplicar rendimentos (para conta poupança)

### 💳 Cartão

- `POST /cartoes` — Emitir um novo cartão  
- `GET /cartoes/{id}` — Obter detalhes de um cartão  
- `POST /cartoes/{id}/pagamento` — Realizar um pagamento com o cartão  
- `PUT /cartoes/{id}/limite` — Alterar limite do cartão  
- `PUT /cartoes/{id}/status` — Ativar ou desativar um cartão  
- `PUT /cartoes/{id}/senha` — Alterar senha do cartão  
- `GET /cartoes/{id}/fatura` — Consultar fatura do cartão de crédito  
- `POST /cartoes/{id}/fatura/pagamento` — Realizar pagamento da fatura do cartão de crédito  
- `PUT /cartoes/{id}/limite-diario` — Alterar limite diário do cartão de débito
