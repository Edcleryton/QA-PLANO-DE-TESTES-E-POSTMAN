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
Este relatório documenta os resultados dos testes realizados na API Restful-Booker. Ele abrange os bugs encontrados, melhorias sugeridas e análises de riscos, com foco em garantir a qualidade da aplicação.

---

## 2. Resumo dos Resultados

- **Total de Casos de Teste Executados:** 11  
  - **Casos Funcionais:** 9  
  - **Casos Não Funcionais:** 2  
- **Casos de Teste Aprovados:** 7  
- **Casos de Teste Reprovados:** 4  
- **Cobertura de Testes:** 100%  
- **Evidências dos Testes:**  
  - **Funcionais:** [Evidências Funcionais](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  
  - **Não Funcionais:** [Evidências Não Funcionais](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Título**                                   | **Gravidade** | **Evidência**                                                                                       | **Status** |
|------------|---------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|------------|
| BUG-0001   | Código de status incorreto para autenticação inválida | Moderada      | [Evidência](./evidencias/BUG-0001-autenticacao-invalida.png)                                        | Aberto     |
| BUG-0002   | Falha ao buscar reserva específica: ID inexistente após criação | Alta          | [Evidência](./evidencias/BUG-0002-id-nao-persistente.png)                                           | Aberto     |
| BUG-0003   | Detalhes da reserva ausentes na resposta          | Alta          | [Evidência](./evidencias/BUG-0003-detalhes-ausentes.png)                                            | Aberto     |
| BUG-0004   | Tipo de conteúdo incorreto na resposta            | Moderada      | [Evidência](./evidencias/BUG-0004-content-type-incorreto.png)                                       | Aberto     |
| BUG-0005   | Dados da reserva inválidos ou ausentes na resposta | Moderada      | [Evidência](./evidencias/BUG-0005-dados-invalidos.png)                                              | Aberto     |
| BUG-0006   | Resposta vazia ao buscar reservas com múltiplos filtros | Alta          | [Evidência](./evidencias/BUG-0006-multiplos-filtros.png)                                            | Aberto     |
| BUG-0007   | Resposta vazia ao buscar reservas por `firstname`  | Alta          | [Evidência](./evidencias/BUG-0007-firstname-vazio.png)                                              | Aberto     |

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
> **Nota:** Consulte o [Plano de Testes](./plano-de-testes.md) para informações detalhadas sobre os casos de teste.
