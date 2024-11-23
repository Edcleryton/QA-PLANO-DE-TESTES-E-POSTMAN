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
Este relatório documenta os resultados dos testes realizados no Sauce Demo e na API Restful-Booker, incluindo bugs encontrados, melhorias sugeridas e análises de riscos.

---

## 2. Resumo dos Resultados

- **Total de Casos de Teste Executados:** 59  
  - **Casos Funcionais:** 40  
  - **Casos Não Funcionais:** 19  
- **Casos de Teste Aprovados:** 50  
- **Casos de Teste Reprovados:** 9  
- **Cobertura de Testes:** 100%

---

## 3. Lista de Bugs Encontrados

| ID       | Descrição                                              | Gravidade | Evidência                   | Status  |
|----------|--------------------------------------------------------|-----------|-----------------------------|---------|
| BUG-001  | Tempo de resposta no login acima do esperado (3.54s)   | Alta      | [Evidência](#)https://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw              | Aberto  |
| BUG-002  | Mensagem de erro genérica ao falhar login              | Moderada  | [Evidência](#)https://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw              | Aberto  |
| BUG-003  | Não sincronização de carrinho entre abas simultâneas   | Moderada  | [Evidência](#)https://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw              | Aberto  |
| BUG-004  | Login não funcional em dispositivos móveis             | Alta      | [Evidênciahttps://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw](#)https://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw              | Aberto  |
| BUG-005  | Navegação para páginas inexistentes sem mensagem clara | Baixa     | [Evidência](#)https://terabox.com/s/1uzW-zoU1QIQk6xu0yUvAyw             | Aberto  |

---

## 4. Sugestões de Melhorias

### **Interface do Usuário (UI):**
- Melhorar a clareza das mensagens de erro para login inválido.
- Adicionar feedback visual ao tentar logar (ex.: loading spinner).

### **Performance:**
- Otimizar o tempo de resposta do endpoint de login para ficar abaixo de 2 segundos.

### **Acessibilidade:**
- Garantir que o site seja compatível com leitores de tela e navegadores por teclado.

---

## 5. Análise de Riscos

| Risco                                                    | Probabilidade | Impacto       | Mitigação                            |
|----------------------------------------------------------|---------------|---------------|--------------------------------------|
| Frustração do usuário devido a mensagens de erro genéricas | Alta          | Alta          | Melhorar mensagens de erro.          |
| Falhas em picos de acesso devido ao desempenho do login  | Média         | Alta          | Otimizar endpoints críticos.         |
| Dificuldade de acesso em dispositivos móveis             | Alta          | Alta          | Testar e ajustar a responsividade.   |

---

## 6. Conclusão e Próximos Passos

### **Conclusão**
Os testes realizados evidenciaram áreas de melhoria que podem impactar diretamente a experiência do usuário e a confiabilidade do sistema.

### **Próximos Passos**
1. Corrigir os bugs identificados.
2. Reexecutar os testes após as correções.
3. Implementar as sugestões de melhorias para UI, desempenho e acessibilidade.
4. Ampliar os testes para incluir novos fluxos identificados como críticos.

---

**Links Úteis:**  
- **Bugs:** [Link para Evidências](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)  
- **Testes Funcionais:** [Link para Evidências](https://terabox.com/s/11J0NPRZJ7hfTIFhCHSMfJA)  
- **Testes Não Funcionais:** [Link para Evidências](https://terabox.com/s/16JvzuwtzvLmdz5cCKArzOw)  
