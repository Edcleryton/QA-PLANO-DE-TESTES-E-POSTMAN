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

- **Total de Casos de Teste Executados:** 55  
  - **Casos Funcionais:** 40  
  - **Casos Não Funcionais:** 15  
- **Casos de Teste Aprovados:** 43  
- **Casos de Teste Reprovados:** 12  
- **Cobertura de Testes:** 100%  
- **Evidências dos Testes:**  
  - **Funcionais:** [Link para Evidências](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  
  - **Não Funcionais:** [Link para Evidências](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)  

---

## 3. Lista de Bugs Encontrados

| **ID**     | **Título**                                  | **Gravidade** | **Evidência**                                                                                       | **Status** |
|------------|--------------------------------------------|---------------|-----------------------------------------------------------------------------------------------------|------------|
| BUG-0001   | Tempo de resposta no login acima do esperado (3.54s) | Alta          | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0002   | Mensagem de erro genérica ao falhar login  | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0003   | Login não funcional em dispositivos móveis | Alta          | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0004   | Login com falha de layout                 | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0005   | Checkout incompleto - Falta de validação obrigatória | Crítica        | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0006   | Ausência de opções de pagamento no checkout | Crítica        | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0007   | Redirecionamento externo não esperado na página "About" | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0008   | Finalização de compra com carrinho vazio   | Crítica        | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0009   | Acessibilidade inadequada na remoção de itens do carrinho | Alta          | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0010   | Falha na opção "Reset App State"           | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0011   | Logout em múltiplas sessões não sincronizado | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0012   | Falta de funcionalidade para alterar quantidade de itens no carrinho | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |
| BUG-0013   | Mensagem de erro ao tentar acessar páginas sem login | Moderada      | [Evidência](https://terabox.com/s/1VPkxVZ8I4vTvC2nnobsJ-g)                                          | Aberto     |

---

## 4. Sugestões de Melhorias

### **Interface do Usuário (UI):**
- Melhorar a clareza das mensagens de erro para login inválido.
- Adicionar feedback visual ao tentar logar (ex.: loading spinner).
- Ajustar alinhamento dos elementos da página de login.

### **Performance:**
- Otimizar o tempo de resposta do endpoint de login para ficar abaixo de 2 segundos.
- Melhorar sincronização de dados entre múltiplas abas.

### **Checkout:**
- Implementar validação obrigatória para todos os campos de pagamento no checkout.
- Adicionar opções de pagamento (cartão de crédito, boleto, etc.).
- Implementar funcionalidade para alterar quantidade de itens diretamente no carrinho.

### **Acessibilidade:**
- Garantir que o site seja compatível com leitores de tela e navegadores por teclado.
- Implementar ajustes para responsividade em dispositivos móveis.
- Garantir foco visível e claro para campos de entrada e botões em todas as páginas.
- Melhorar foco e usabilidade ao remover itens do carrinho usando o teclado.

---

## 5. Análise de Riscos

| **Risco**                                                 | **Probabilidade** | **Impacto**      | **Mitigação**                           |
|-----------------------------------------------------------|-------------------|------------------|-----------------------------------------|
| Frustração do usuário devido a mensagens de erro genéricas | Alta              | Alta             | Melhorar mensagens de erro.             |
| Falhas em picos de acesso devido ao desempenho do login   | Média             | Alta             | Otimizar endpoints críticos.            |
| Dificuldade de acesso em dispositivos móveis              | Alta              | Alta             | Ajustar layout e compatibilidade móvel. |
| Finalização de compra sem validação obrigatória           | Alta              | Alta             | Implementar validação de todos os campos no checkout. |
| Navegação ambígua para páginas externas                   | Média             | Moderada         | Revisar redirecionamentos no menu e páginas. |

---

## 6. Conclusão e Próximos Passos

### **Conclusão**
Os testes realizados destacaram áreas críticas que precisam de melhorias para proporcionar uma experiência de usuário confiável e eficiente. 

### **Próximos Passos**
1. **Correção dos Bugs Identificados:** Resolver todos os bugs priorizando os de maior criticidade.  
2. **Execução de Retestes:** Reexecutar os testes para garantir a eficácia das correções.  
3. **Implementação de Melhorias:** Foco na otimização de UI, performance, checkout e acessibilidade.  
4. **Expansão dos Testes:** Ampliar os testes para novos fluxos e cenários críticos.  

---

> **Nota:** Consulte o [Registro de Bugs](./registro-de-bugs.md) para mais detalhes sobre os bugs identificados.  
> **Nota:** Consulte o [Plano de Testes](./plano-de-testes.md) para informações detalhadas sobre os casos de teste.
