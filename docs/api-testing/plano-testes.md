# Plano de Testes - Restful-Booker 

## Índice

1. [Introdução](#introdução)
2. [Escopo](#escopo)
3. [Ferramentas de Testes](#ferramentas-de-testes)
4. [Estratégias de Testes](#estratégias-de-testes)
5. [Cronograma](#cronograma)
6. [Cenários de Testes](#cenários-de-testes)
   - 6.1 [Autenticação](#61-autenticação)
     - 6.1.1 [Testes Funcionais](#611-testes-funcionais)
   - 6.2 [Gestão de Reservas](#62-gestão-de-reservas)
     - 6.2.1 [Testes Funcionais](#621-testes-funcionais)
   - 6.3 [Filtros e Buscas](#63-filtros-e-buscas)
     - 6.3.1 [Testes Funcionais](#631-testes-funcionais)

---

## 1. Introdução

Este plano de testes foi desenvolvido para garantir a qualidade da API Restful-Booker. Ele cobre testes funcionais e não funcionais, priorizando a validação de autenticação, gestão de reservas e filtros de busca.

---

## 2. Escopo

- **API Testing (Restful-Booker):**
  - Testar endpoints principais, incluindo autenticação, criação, atualização e deleção de reservas.
  - Garantir que os filtros funcionem corretamente, retornando os dados esperados.
  - Validar comportamento em cenários de erro, como autenticação com credenciais inválidas e filtros inválidos.

---

## 3. Ferramentas de Testes

- **API Testing:**
  - Postman
  - Variáveis de ambiente configuradas para URL e parâmetros dinâmicos

---

## 4. Estratégias de Testes

- **Testes Funcionais:** Validação dos endpoints principais e fluxos críticos.
- **Testes Não Funcionais:** Verificação de tempos de resposta e comportamento sob carga.

---

## 5. Cronograma

| Atividade             | Duração | Data de Início | Data de Término |
|-----------------------|---------|----------------|-----------------|
| Planejar Testes       | 1 dia   | 24/11/2024     | 24/11/2024      |
| Criar Casos de Teste  | 1 dia   | 24/11/2024     | 24/11/2024      |
| Executar Testes       | 1 dia   | 25/11/2024     | 25/11/2024      |
| Documentar Resultados | 1 dia   | 25/11/2024     | 25/11/2024      |

---

## 6. Cenários de Testes

### 6.1 Autenticação

#### 6.1.1 Testes Funcionais

| **ID**   | **Descrição**                                | **Passos para Reproduzir**                                                                                                                                                                                       | **Resultado Esperado**                                                                                                 |
|----------|----------------------------------------------|-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| AU-001   | Gerar token com credenciais válidas          | 1. Realizar uma requisição **POST** no endpoint `/auth`.<br>2. Enviar credenciais válidas no corpo da requisição (`username`: `admin`, `password`: `password123`).                                                | Retornar código de status **200** com o token gerado.                                                                  |
| AU-002   | Tentar gerar token com credenciais inválidas | 1. Realizar uma requisição **POST** no endpoint `/auth`.<br>2. Enviar credenciais inválidas no corpo da requisição (`username`: `invalidUser`, `password`: `invalidPass`).                                         | Retornar código de status **401 Unauthorized** com a mensagem `"reason": "Bad credentials"`. **Bug encontrado:** Retorna **200 OK**. |

---

### 6.2 Gestão de Reservas

#### 6.2.1 Testes Funcionais

| **ID**   | **Descrição**                  | **Passos para Reproduzir**                                                                                                                                                                                         | **Resultado Esperado**                                                                                     |
|----------|--------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------|------------------------------------------------------------------------------------------------------------|
| GR-001   | Criar uma nova reserva         | 1. Realizar uma requisição **POST** no endpoint `/booking`.<br>2. Enviar os dados da reserva no corpo da requisição (ex.: `firstname`, `lastname`, `totalprice`, `depositpaid`, `bookingdates`, `additionalneeds`). | Retornar código de status **200** com o ID da reserva e detalhes criados.                                  |
| GR-002   | Buscar uma reserva específica  | 1. Realizar uma requisição **GET** no endpoint `/booking/{id}`.<br>2. Informar um **ID válido** na URL.                                                                                                             | Retornar código de status **200** com os detalhes da reserva.                                              |
| GR-003   | Listar todas as reservas       | 1. Realizar uma requisição **GET** no endpoint `/booking`.                                                                                                                                                          | Retornar código de status **200** com a lista de IDs de reservas.                                          |
| GR-004   | Atualizar uma reserva existente | 1. Realizar uma requisição **PUT** no endpoint `/booking/{id}`.<br>2. Enviar novos dados da reserva no corpo da requisição.<br>3. Incluir o token de autenticação nos headers.                                     | Retornar código de status **200** com os dados atualizados.                                                |
| GR-005   | Deletar uma reserva            | 1. Realizar uma requisição **DELETE** no endpoint `/booking/{id}`.<br>2. Informar um **ID válido** na URL.<br>3. Incluir o token de autenticação nos headers.                                                       | Retornar código de status **201** confirmando a deleção da reserva.                                        |

---

### 6.3 Filtros e Buscas

#### 6.3.1 Testes Funcionais

| **ID**   | **Descrição**                        | **Passos para Reproduzir**                                                                                                                                             | **Resultado Esperado**                                                                                       |
|----------|--------------------------------------|------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------------------------|
| FB-001   | Buscar reservas por nome             | 1. Realizar uma requisição **GET** no endpoint `/booking?firstname={nome}`.<br>2. Informar um nome válido no parâmetro `firstname`.                                    | Retornar código de status **200** com as reservas correspondentes ao nome informado.                          |
| FB-002   | Buscar reservas por data de check-in | 1. Realizar uma requisição **GET** no endpoint `/booking?checkin={data}`.<br>2. Informar uma data válida no parâmetro `checkin` no formato `YYYY-MM-DD`.               | Retornar código de status **200** com as reservas correspondentes à data de check-in informada.              |
| FB-003   | Buscar reservas por data de check-out | 1. Realizar uma requisição **GET** no endpoint `/booking?checkout={data}`.<br>2. Informar uma data válida no parâmetro `checkout` no formato `YYYY-MM-DD`.             | Retornar código de status **200** com as reservas correspondentes à data de check-out informada.             |
| FB-004   | Buscar reservas com múltiplos filtros | 1. Realizar uma requisição **GET** no endpoint `/booking` com múltiplos parâmetros (ex.: `firstname`, `checkin`, `checkout`).                                          | Retornar código de status **200** com as reservas que atendem a todos os filtros aplicados.                  |

---
