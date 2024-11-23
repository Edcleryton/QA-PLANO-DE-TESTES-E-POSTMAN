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
- **Total de Casos de Teste Executados**: 10
- **Casos de Teste Aprovados**: 8
- **Casos de Teste Reprovados**: 2
- **Cobertura de Testes**: 100%

---

## 3. Lista de Bugs Encontrados

| ID       | Descrição                                     | Gravidade      | Evidência                         | Status      |
|----------|---------------------------------------------|----------------|-----------------------------------|-------------|
| BUG-001  | Tempo de resposta no login acima do esperado (3.54s) | Alta           | [Evidência](#)                    | Aberto      |
| BUG-002  | Mensagem de erro genérica ao falhar login   | Moderada       | [Evidência](#)                    | Aberto      |

---

## 4. Sugestões de Melhorias
1. **Interface do Usuário (UI):**
   - Melhorar a clareza das mensagens de erro para login inválido.
   - Adicionar feedback visual ao tentar logar (ex.: loading spinner).

2. **Performance:**
   - Otimizar o tempo de resposta do endpoint de login para ficar abaixo de 2 segundos.

3. **Acessibilidade:**
   - Garantir que o site seja compatível com leitores de tela e navegadores por teclado.

---

## 5. Análise de Riscos
- Risco de frustração do usuário devido a mensagens de erro genéricas.
- Possibilidade de falhas em picos de acesso devido ao desempenho do login.

---

## 6. Conclusão e Próximos Passos
- **Conclusão:** Os testes evidenciaram pontos de melhoria que podem impactar a experiência do usuário.
- **Próximos Passos:**
  1. Corrigir os bugs identificados.
  2. Executar novos testes após correções.
