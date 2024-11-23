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
Este relatório documenta os resultados dos testes realizados no Sauce Demo e na API Restful-Booker, abrangendo bugs encontrados, melhorias sugeridas e análises de riscos, com foco em garantir a qualidade da aplicação.

---

## 2. Resumo dos Resultados

- **Total de Casos de Teste Executados:** 59  
  - **Casos Funcionais:** 40  
  - **Casos Não Funcionais:** 19  
- **Casos de Teste Aprovados:** 50  
- **Casos de Teste Reprovados:** 9  
- **Cobertura de Testes:** 100%  
- **Evidências dos Testes:**  
  - **Funcionais:** [Link para Evidências](https://terabox.com/s/11J0NPRZJ7hfTIFhCHSMfJA)  
  - **Não Funcionais:** [Link para Evidências](https://terabox.com/s/16JvzuwtzvLmdz5cCKArzOw)  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Título**                                  | **Gravidade** | **Evidência**                                                                                       | **Status** |
|------------|--------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|------------|
| BUG-0001   | Tempo de resposta no login acima do esperado (3.54s) | Alta          | [Evidência](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)                                          | Aberto     |
| BUG-0002   | Mensagem de erro genérica ao falhar login  | Moderada      | [Evidência](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)                                          | Aberto     |
| BUG-0003   | Não sincronização de carrinho entre abas simultâneas | Moderada      | [Evidência](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)                                          | Aberto     |
| BUG-0004   | Login não funcional em dispositivos móveis | Alta          | [Evidência](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)                                          | Aberto     |

---

## 4. Sugestões de Melhorias

### **Interface do Usuário (UI):**
- Melhorar a clareza das mensagens de erro para login inválido.
- Adicionar feedback visual ao tentar logar (ex.: loading spinner).

### **Performance:**
- Otimizar o tempo de resposta do endpoint de login para ficar abaixo de 2 segundos.
- Melhorar sincronização de dados entre múltiplas abas.

### **Acessibilidade:**
- Garantir que o site seja compatível com leitores de tela e navegadores por teclado.
- Implementar ajustes para responsividade em dispositivos móveis.

---

## 5. Análise de Riscos

| **Risco**                                                 | **Probabilidade** | **Impacto**      | **Mitigação**                           |
|-----------------------------------------------------------|-------------------|------------------|-----------------------------------------|
| Frustração do usuário devido a mensagens de erro genéricas | Alta              | Alta             | Melhorar mensagens de erro.             |
| Falhas em picos de acesso devido ao desempenho do login   | Média             | Alta             | Otimizar endpoints críticos.            |
| Dificuldade de acesso em dispositivos móveis              | Alta              | Alta             | Ajustar layout e compatibilidade móvel. |

---

## 6. Conclusão e Próximos Passos

### **Conclusão**
Os testes realizados destacaram áreas críticas que precisam de melhorias para proporcionar uma experiência de usuário confiável e eficiente. 

### **Próximos Passos**
1. **Correção dos Bugs Identificados:** Resolver todos os bugs priorizando os de maior criticidade.  
2. **Execução de Retestes:** Reexecutar os testes para garantir a eficácia das correções.  
3. **Implementação de Melhorias:** Foco na otimização de UI, performance e acessibilidade.  
4. **Expansão dos Testes:** Ampliar os testes para novos fluxos e cenários críticos.  

---

**Links Relacionados:**  
- **Bugs:** [Registro de Bugs](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)  
- **Testes Funcionais:** [Evidências Funcionais](https://terabox.com/s/11J0NPRZJ7hfTIFhCHSMfJA)  
- **Testes Não Funcionais:** [Evidências Não Funcionais](https://terabox.com/s/16JvzuwtzvLmdz5cCKArzOw)  
