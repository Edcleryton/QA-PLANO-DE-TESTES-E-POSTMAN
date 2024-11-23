# Relatório de Resultados - Sauce Demo e Restful-Booker

## Índice
1. [Introdução](#introdução)  
2. [Resumo dos Resultados](#resumo-dos-resultados)  
3. [Lista de Bugs Encontrados](#lista-de-bugs-encontrados)  
4. [Sugestões de Melhorias](#sugestões-de-melhorias)  
5. [Análise de Riscos](#análise-de-riscos)  
6. [Conclusão e Próximos Passos](#conclusão-e-próximos-passos)  

---

## 1. Introdução

Este relatório documenta os resultados dos testes realizados no **Sauce Demo** e na API **Restful-Booker**, incluindo bugs encontrados, melhorias sugeridas e análises de riscos. Ele fornece uma visão geral da qualidade do sistema testado e aponta os principais desafios encontrados.

---

## 2. Resumo dos Resultados

- **Total de Casos de Teste Executados:** 15  
- **Casos de Teste Aprovados:** 12  
- **Casos de Teste Reprovados:** 3  
- **Cobertura de Testes:** 100%  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Descrição**                                   | **Gravidade** | **Evidência**                                           | **Status** |
|------------|------------------------------------------------|---------------|--------------------------------------------------------|------------|
| BUG-001    | Tempo de resposta no login acima do esperado (3.54s) | Alta          | [Evidência BUG-001](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ) | Aberto     |
| BUG-002    | Mensagem de erro genérica ao falhar login       | Moderada      | [Evidência BUG-002](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ) | Aberto     |
| BUG-003    | Sincronização de itens no carrinho entre abas não ocorre automaticamente | Alta | [Evidência BUG-003](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ) | Aberto |
| BUG-004    | Site não carrega em dispositivos móveis (POCO X6 PRO, Android 14, Brave e Chrome) | Alta | [Evidência BUG-004](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ) | Aberto |

---

## 4. Sugestões de Melhorias

### **Interface do Usuário (UI):**
- Melhorar a clareza das mensagens de erro para login inválido.
- Adicionar feedback visual ao tentar logar (ex.: loading spinner).
- Implementar sincronização automática de itens entre múltiplas abas.

### **Performance:**
- Otimizar o tempo de resposta do endpoint de login para ficar abaixo de 2 segundos.

### **Acessibilidade:**
- Garantir que o site seja compatível com leitores de tela e navegadores por teclado.
- Ajustar layout responsivo para carregamento correto em dispositivos móveis.

---

## 5. Análise de Riscos

| **Risco**                                              | **Impacto**          | **Mitigação**                                              |
|--------------------------------------------------------|----------------------|-----------------------------------------------------------|
| Frustração do usuário devido a mensagens de erro genéricas | Alta                 | Personalizar mensagens para serem claras e específicas.   |
| Possibilidade de falhas em picos de acesso devido ao desempenho do login | Alta                 | Implementar melhorias no desempenho do backend e escalabilidade. |
| Perda de vendas por falhas em dispositivos móveis       | Alta                 | Ajustar layout e funcionalidade para compatibilidade universal. |
| Inconsistências ao navegar com múltiplas abas abertas   | Média                | Sincronizar o estado do carrinho em tempo real.           |

---

## 6. Conclusão e Próximos Passos

### **Conclusão:**
Os testes evidenciaram pontos de melhoria significativos que podem impactar negativamente a experiência do usuário e a confiabilidade do sistema em momentos críticos.

### **Próximos Passos:**
1. Corrigir os bugs identificados, priorizando o desempenho do login, mensagens de erro e layout responsivo.  
2. Implementar a sincronização automática do estado do carrinho entre abas.  
3. Executar novos testes após as correções para validar as melhorias implementadas.  
4. Realizar uma revisão final com foco em acessibilidade e usabilidade.  

---

**Links Importantes:**  
- 🔗 [Evidências de Testes Funcionais](https://terabox.com/s/11J0NPRZJ7hfTIFhCHSMfJA)  
- 🔗 [Evidências de Testes Não Funcionais](https://terabox.com/s/16JvzuwtzvLmdz5cCKArzOw)  
- 🔗 [Evidências de Bugs](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)  

---
