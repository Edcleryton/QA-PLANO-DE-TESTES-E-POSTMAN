# Relatório de Resultados - Restful-Booker

## Índice
1. [Introdução](#introdução)  
2. [Resumo dos Resultados](#resumo-dos-resultados)  
3. [Lista de Bugs Encontrados](#lista-de-bugs-encontrados)  
4. [Sugestões de Melhorias](#sugestões-de-melhorias)  
5. [Análise de Riscos](#análise-de-riscos)  
6. [Conclusão e Próximos Passos](#conclusão-e-próximos-passos)  

---

## 1. Introdução

Este relatório documenta os resultados dos testes realizados na API Restful-Booker. Ele abrange os bugs encontrados, melhorias sugeridas e análises de riscos, com foco em garantir a qualidade da aplicação. Além disso, todas as evidências dos testes são baseadas no código e na collection JSON disponível no repositório.

---

## 2. Resumo dos Resultados

- **Total de Casos de Teste Executados:** 11  
  - **Casos Funcionais:** 9  
  - **Casos Não Funcionais:** 2  
- **Casos de Teste Aprovados:** 7  
- **Casos de Teste Reprovados:** 4  
- **Cobertura de Testes:** 100%  
- **Evidências dos Testes:**  
  - A collection JSON utilizada para os testes está disponível [aqui](https://github.com/Edcleryton/QA-Testing-BeTalent/blob/main/docs/api-testing/API%20Testing%20(Restful-Booker).postman_collection.json).  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Título**                                   | **Gravidade** | **Evidência**                                                                                       | **Status** |
|------------|---------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|------------|
| BUG-0001   | Código de status incorreto para autenticação inválida | Moderada      | [Registro de Bugs - BUG-0001](./registro-de-bugs.md#bug-0001)                                        | Aberto     |
| BUG-0002   | Falha ao buscar reserva específica: ID inexistente após criação | Alta          | [Registro de Bugs - BUG-0002](./registro-de-bugs.md#bug-0002)                                       | Aberto     |
| BUG-0003   | Detalhes da reserva ausentes na resposta          | Alta          | [Registro de Bugs - BUG-0003](./registro-de-bugs.md#bug-0003)                                       | Aberto     |
| BUG-0004   | Tipo de conteúdo incorreto na resposta            | Moderada      | [Registro de Bugs - BUG-0004](./registro-de-bugs.md#bug-0004)                                       | Aberto     |
| BUG-0005   | Dados da reserva inválidos ou ausentes na resposta | Moderada      | [Registro de Bugs - BUG-0005](./registro-de-bugs.md#bug-0005)                                       | Aberto     |
| BUG-0006   | Resposta vazia ao buscar reservas com múltiplos filtros | Alta          | [Registro de Bugs - BUG-0006](./registro-de-bugs.md#bug-0006)                                       | Aberto     |
| BUG-0007   | Resposta vazia ao buscar reservas por `firstname`  | Alta          | [Registro de Bugs - BUG-0007](./registro-de-bugs.md#bug-0007)                                       | Aberto     |

---

## 4. Sugestões de Melhorias

### **Autenticação:**
- Ajustar o código de status para autenticação inválida de **200 OK** para **401 Unauthorized**.
- Melhorar a mensagem de erro para ser mais informativa e clara.

### **Gestão de Reservas:**
- Garantir a persistência dos IDs das reservas após a criação.
- Garantir que os detalhes das reservas sejam retornados de forma consistente.

### **Filtros e Buscas:**
- Corrigir os filtros para que retornem reservas correspondentes aos critérios aplicados.
- Implementar validações para evitar respostas vazias quando há dados disponíveis.

### **Observação Importante:**
- É necessário gerar um novo token de autenticação a cada 15 minutos para realizar os testes dos endpoints GR-004 e GR-005.

---

## 5. Análise de Riscos

| **Risco**                                                | **Probabilidade** | **Impacto**      | **Mitigação**                            |
|----------------------------------------------------------|-------------------|------------------|------------------------------------------|
| Respostas de status inconsistentes em autenticação       | Alta              | Alta             | Ajustar as respostas de código de status nos endpoints de autenticação. |
| Falha de persistência de dados                           | Alta              | Alta             | Revisar a lógica de persistência das reservas após criação. |
| Respostas vazias em filtros e buscas                     | Alta              | Alta             | Implementar validações e ajustes nos filtros de busca. |

---

## 6. Conclusão e Próximos Passos

### **Conclusão**
Os testes realizados identificaram diversos bugs de alta severidade relacionados à persistência, filtros e consistência nos dados retornados pela API. Esses problemas impactam diretamente a experiência do usuário e a confiabilidade do sistema.

### **Próximos Passos**
1. **Correção dos Bugs Identificados:** Resolver os problemas de persistência, filtros e consistência nos dados.  
2. **Execução de Retestes:** Garantir que as correções aplicadas resolvam os problemas sem introduzir novos erros.  
3. **Validação Final:** Revalidar todos os cenários de autenticação, reservas e filtros antes de concluir os testes.  

---

> **Nota:** Consulte o [Registro de Bugs](./registro-de-bugs.md) para mais detalhes sobre os bugs identificados.  
> **Nota:** Consulte o [Plano de Testes](./plano-testes.md) para informações detalhadas sobre os casos de teste.
