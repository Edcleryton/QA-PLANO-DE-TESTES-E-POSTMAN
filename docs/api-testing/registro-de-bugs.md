# Registro de Bugs Restful-Booker

## Índice
1. [Detalhes dos Bugs](#detalhes-dos-bugs)  
2. [Resumo Geral](#resumo-geral)  

---

## Detalhes dos Bugs

| **ID**      | **Título**                                         | **Passo-a-passo**                                                                                                                                                           | **Objetivo**                                                                                | **Versão** | **Plataforma** | **Navegador**     | **Criticidade** | **Status** | **Evidência**                                                                                              | **Caso de Teste Relacionado** |
|-------------|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------|----------------|-------------------|-----------------|------------|------------------------------------------------------------------------------------------------------------|--------------------------------|
| BUG-0001    | Código de status incorreto ao autenticar com credenciais inválidas | **Dado:** que o usuário tenta autenticar na API com credenciais inválidas.<br>**Quando:** realiza a requisição para o endpoint `/auth` com username e password incorretos.<br>**Então:** o código de status retornado é `200 OK`, mas deveria ser `401 Unauthorized`. | Garantir que a API retorne o código de status correto (`401 Unauthorized`) para autenticação inválida. | 1          | Windows        | Postman           | Moderada        | Aberto     | ![Evidência](./evidencias/BUG-0001-autenticacao-invalida.png)                                               | Teste de Autenticação Invalida |
| BUG-0002    | ID de reserva não persiste após criação           | **Dado:** que o usuário cria uma nova reserva via `POST /booking`.<br>**Quando:** a API retorna o ID da reserva criada.<br>**E:** o usuário tenta buscar a reserva usando `GET /booking/{id}` imediatamente.<br>**Então:** o código de status retornado é `404 Not Found`, mas deveria ser `200 OK`. | Garantir que a API persista corretamente os dados da reserva criada.                         | 1          | Windows        | Postman           | Alta            | Aberto     | ![Evidência](./evidencias/BUG-0002-id-nao-persiste.png)                                                    | Teste de Criação e Consulta de Reservas |

---

## Resumo Geral

- **Total de Bugs Registrados:** 2  
- **Bugs Críticos/Bloqueadores:** 1  
- **Bugs Moderados:** 1  
- **Bugs Leves:** 0  
- **Status Atual dos Bugs:**  
  - **Abertos:** 2  
  - **Fechados:** 0  

### Notas Adicionais
- **BUG-0001:** Afeta diretamente a consistência do comportamento da API, mas não impede seu funcionamento geral.
- **BUG-0002:** Afeta a persistência dos dados, impossibilitando a gestão das reservas criadas.

### Próximos Passos
1. **BUG-0001:** Corrigir o retorno do código de status para refletir a resposta esperada (`401 Unauthorized`) em casos de autenticação inválida.
2. **BUG-0002:** Verificar a lógica de persistência no backend da API para garantir que os dados das reservas criadas sejam armazenados corretamente.

> **Nota:** Consulte o [Plano de Testes](./plano-testes.md) e o [Relatório de Resultados](./relatorio-resultados.md) para mais detalhes.





