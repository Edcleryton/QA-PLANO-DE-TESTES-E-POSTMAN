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

- **Total de Casos de Teste Executados:** 9  
  - **Casos Funcionais:** 6  
  - **Casos Não Funcionais:** 3  
- **Casos de Teste Aprovados:** 8  
- **Casos de Teste Reprovados:** 1  
- **Cobertura de Testes:** 100%  
- **Evidências dos Testes:**  
  - **Funcionais:** [Evidências Funcionais](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  
  - **Não Funcionais:** [Evidências Não Funcionais](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Título**                                   | **Gravidade** | **Evidência**                                                                                       | **Status** |
|------------|---------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|------------|
| BUG-0001   | Código de status incorreto para autenticação inválida | Alta          | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |

---

## 4. Sugestões de Melhorias

### **Autenticação:**
- Ajustar o código de status para autenticação inválida de **200 OK** para **401 Unauthorized**.
- Melhorar a mensagem de erro para ser mais informativa e clara.

### **Performance:**
- Garantir que o tempo de resposta para geração de token esteja abaixo de 2 segundos.

---

## 5. Análise de Riscos

| **Risco**                                                | **Probabilidade** | **Impacto**      | **Mitigação**                            |
|----------------------------------------------------------|-------------------|------------------|------------------------------------------|
| Respostas de status inconsistentes em autenticação       | Alta              | Alta             | Ajustar as respostas de código de status nos endpoints de autenticação. |

---

## 6. Conclusão e Próximos Passos

### **Conclusão**
Os testes realizados identificaram um bug crítico relacionado à autenticação inválida. Este problema impacta diretamente a experiência do usuário e a consistência do sistema.

### **Próximos Passos**
1. **Correção do Bug Identificado:** Resolver o problema de código de status no endpoint de autenticação.  
2. **Execução de Retestes:** Garantir que as correções aplicadas resolvam o problema sem introduzir novos erros.  
3. **Validação Final:** Revalidar todos os cenários de autenticação antes de prosseguir para os testes de reservas e filtros.  

---

> **Nota:** Consulte o [Registro de Bugs](./registro-de-bugs.md) para mais detalhes sobre o bug identificado.  
> **Nota:** Consulte o [Plano de Testes](./plano-de-testes.md) para informações detalhadas sobre os casos de teste.

