# Registro de Bugs Restful-Booker

## Índice
1. [Detalhes dos Bugs](#detalhes-dos-bugs)  
2. [Resumo Geral](#resumo-geral)  

---

## Detalhes dos Bugs

| **ID**      | **Título**                                         | **Passo-a-passo**                                                                                                                                                           | **Objetivo**                                                                                | **Versão** | **Plataforma** | **Navegador**     | **Criticidade** | **Status** | **Evidência**                                                                                              | **Caso de Teste Relacionado** |
|-------------|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------|----------------|-------------------|-----------------|------------|------------------------------------------------------------------------------------------------------------|--------------------------------|
| BUG-0001    | Código de status incorreto ao autenticar com credenciais inválidas | **Dado:** que o usuário tenta autenticar na API com credenciais inválidas.<br>**Quando:** realiza a requisição para o endpoint `/auth` com username e password incorretos.<br>**Então:** o código de status retornado é `200 OK`, mas deveria ser `401 Unauthorized`. | Garantir que a API retorne o código de status correto (`401 Unauthorized`) para autenticação inválida. | 1          | Windows        | Postman           | Moderada        | Aberto     | ![Evidência](./evidencias/BUG-0001-autenticacao-invalida.png)                                               | Teste de Autenticação Invalida |
| BUG-0002    | Falha ao buscar reserva específica: ID inexistente após criação | **Dado:** que o usuário cria uma reserva e recebe um ID.<br>**Quando:** tenta buscar o ID recém-criado no endpoint `/booking/{id}`.<br>**Então:** a API retorna `404 Not Found` em vez de `200 OK`. | Garantir que a API persista os dados da reserva após sua criação.                                | 1          | Windows        | Postman           | Alta            | Aberto     | ![Evidência](./evidencias/BUG-0002-id-nao-persistente.png)                                                 | GR-001 e GR-002 |
| BUG-0003    | Detalhes da reserva ausentes na resposta          | **Dado:** que o usuário busca uma reserva específica.<br>**Quando:** realiza a requisição para o endpoint `/booking/{id}`.<br>**Então:** a resposta não contém os detalhes obrigatórios como `firstname`, `lastname`, `totalprice`, etc. | Garantir que a API retorne todos os detalhes obrigatórios da reserva na resposta.             | 1          | Windows        | Postman           | Alta            | Aberto     | ![Evidência](./evidencias/BUG-0003-detalhes-ausentes.png)                                                  | GR-002 |
| BUG-0004    | Tipo de conteúdo incorreto na resposta            | **Dado:** que o usuário realiza uma requisição para buscar uma reserva.<br>**Quando:** a API responde.<br>**Então:** o cabeçalho `Content-Type` é `text/plain; charset=utf-8` em vez de `application/json`. | Garantir que a API retorne o tipo de conteúdo correto (`application/json`).                     | 1          | Windows        | Postman           | Moderada        | Aberto     | ![Evidência](./evidencias/BUG-0004-content-type-incorreto.png)                                             | GR-002 |
| BUG-0005    | Dados da reserva inválidos ou ausentes na resposta | **Dado:** que o usuário tenta salvar os dados da reserva retornada pela API.<br>**Quando:** a resposta da API é inválida ou não contém os dados esperados.<br>**Então:** o armazenamento para validação futura falha. | Garantir que a API retorne os dados esperados para validação e reaproveitamento.              | 1          | Windows        | Postman           | Moderada        | Aberto     | ![Evidência](./evidencias/BUG-0005-dados-invalidos.png)                                                    | GR-002 |

---

## Resumo Geral

- **Total de Bugs Registrados:** 5  
- **Bugs Críticos/Bloqueadores:** 0  
- **Bugs Moderados:** 3  
- **Bugs Altos:** 2  
- **Status Atual dos Bugs:**  
  - **Abertos:** 5  
  - **Fechados:** 0  

### Notas Adicionais
- **Priorização:** 
  - Os bugs BUG-0002 e BUG-0003 possuem maior impacto e devem ser priorizados.
- **Próximos Passos:** 
  - Corrigir os problemas de persistência e consistência nos dados da API. 
  - Garantir que o tipo de conteúdo esteja alinhado ao esperado (`application/json`).
  - Validar os dados da reserva antes de retornar a resposta.

> **Nota:** Consulte o [Plano de Testes](./plano-testes.md) e o [Relatório de Resultados](./relatorio-resultados.md) para mais detalhes.
