# Registro de Bugs Restful-Booker

## Índice
1. [Detalhes dos Bugs](#detalhes-dos-bugs)  
2. [Resumo Geral](#resumo-geral)  

---

## Detalhes dos Bugs

| **ID**      | **Título**                                         | **Passo-a-passo**                                                                                                                                                           | **Objetivo**                                                                                | **Versão** | **Plataforma** | **Navegador**     | **Criticidade** | **Status** | **Evidência**                                                                                              | **Caso de Teste Relacionado** |
|-------------|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------|----------------|-------------------|-----------------|------------|------------------------------------------------------------------------------------------------------------|--------------------------------|
| BUG-0001    | Código de status incorreto ao autenticar com credenciais inválidas | **Dado:** que o usuário tenta autenticar na API com credenciais inválidas.<br>**Quando:** realiza a requisição para o endpoint `/auth` com username e password incorretos.<br>**Então:** o código de status retornado é `200 OK`, mas deveria ser `401 Unauthorized`. | Garantir que a API retorne o código de status correto (`401 Unauthorized`) para autenticação inválida. | 1          | Windows        | Postman           | Moderada        | Aberto     | ![Evidência](./evidencias/BUG-0001-autenticacao-invalida.png)                                               | Teste de Autenticação Invalida |

---

## Resumo Geral

- **Total de Bugs Registrados:** 1  
- **Bugs Críticos/Bloqueadores:** 0  
- **Bugs Moderados:** 1  
- **Bugs Leves:** 0  
- **Status Atual dos Bugs:**  
  - **Abertos:** 1  
  - **Fechados:** 0  

### Notas Adicionais
- **Priorização:** Este bug afeta diretamente a consistência do comportamento da API, mas não impede seu funcionamento geral.
- **Próximos Passos:** Corrigir o retorno do código de status para refletir a resposta esperada (`401 Unauthorized`).

> **Nota:** Consulte o [Plano de Testes](./plano-testes.md) e o [Relatório de Resultados](./relatorio-resultados.md) para mais detalhes.
