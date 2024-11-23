# Plano de Testes - Sauce Demo e Restful-Booker

## Índice

1. [Introdução](#introdução)  
2. [Escopo](#escopo)  
3. [Ferramentas de Testes](#ferramentas-de-testes)  
4. [Estratégias de Testes](#estratégias-de-testes)  
5. [Cronograma](#cronograma)  
6. [Tipos de Testes](#tipos-de-testes)  
7. [Cenários de Testes](#cenários-de-testes)  

---

## 1. Introdução

Este plano de testes foi desenvolvido para garantir a qualidade das funcionalidades da aplicação Sauce Demo e da API Restful-Booker. Ele cobre testes funcionais e não funcionais, priorizando a experiência do usuário, a acessibilidade e o desempenho.

---

## 2. Escopo

- **UI Testing (Sauce Demo):**
  - Validar os fluxos principais da aplicação, como login, navegação, compra e logout.
  - Verificar responsividade e acessibilidade.

- **API Testing (Restful-Booker):**
  - Testar endpoints para autenticação, gestão de reservas e filtros.

---

## 3. Ferramentas de Testes

- **UI Testing:**
  - Google Chrome
  - Firefox
  - Lighthouse
  - DevTools
  - Selenium

- **API Testing:**
  - Postman
  - Variáveis de ambiente para configuração dinâmica
  - JMeter (para cenários de carga)

- **Controle de Qualidade:**
  - GitHub (armazenamento de evidências)
  - QASE (gerenciamento de casos de teste)

---

## 4. Estratégias de Testes

- **Testes Funcionais:** Validação das principais funcionalidades e fluxos críticos.
- **Testes Não Funcionais:** Verificação de acessibilidade, segurança e desempenho.
- **Documentação:** Casos de teste, evidências, e análise de riscos registrados de forma detalhada.

> **Relatório Complementar:** Os resultados dos testes, bugs encontrados e sugestões de melhorias estão documentados no relatório complementar: [Relatório de Resultados](./relatorio-resultados.md).

---

## 5. Cronograma

| Atividade              | Duração | Data de Início | Data de Término |
|------------------------|---------|----------------|-----------------|
| Planejar Testes        | 1 dia   | 21/11/2024     | 21/11/2024      |
| Criar Casos de Teste   | 2 dias  | 21/11/2024     | 23/11/2024      |
| Executar Testes (UI)   | 2 dias  | 23/11/2024     | 24/11/2024      |
| Executar Testes (API)  | 2 dias  | 24/11/2024     | 25/11/2024      |
| Documentar Resultados  | 1 dia   | 26/11/2024     | 26/11/2024      |

---

## 6. Tipos de Testes

### 6.1 Testes Funcionais
- Validação de fluxos principais como login, navegação, ordenação e checkout.

### 6.2 Testes Não Funcionais
- **Acessibilidade:** Navegação por teclado e leitores de tela.
- **Segurança:** Rejeição de scripts maliciosos.
- **Desempenho:** Medição de tempos de resposta.
- **Responsividade:** Adaptação para dispositivos móveis.

---

## 7. Cenários de Testes

### 7.1 UI Testing (Sauce Demo)

#### 7.1.1 Login com diferentes tipos de usuários

##### 7.1.1.1 Testes Funcionais

| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-001  | Login com credenciais válidas               | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `standard_user`<br>3. Clicar em "Login" | Usuário logado com sucesso e redirecionado para a página inicial. |
| LG-002  | Login com credenciais inválidas             | 1. Acessar a página de login<br>2. Inserir email válido e senha inválida<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando falha no login. |
| LG-003  | Login com campos vazios                     | 1. Acessar a página de login<br>2. Deixar os campos "Username" e "Password" vazios<br>3. Clicar em "Login" | Exibição de mensagem de erro solicitando preenchimento dos campos obrigatórios. |
| LG-004  | Login com nome de usuário inexistente       | 1. Acessar a página de login<br>2. Inserir nome de usuário não cadastrado<br>3. Inserir senha válida<br>4. Clicar em "Login" | Exibição de mensagem de erro informando que o usuário não existe. |
| LG-005  | Login com senha vazia                       | 1. Acessar a página de login<br>2. Inserir um nome de usuário válido<br>3. Deixar o campo de senha vazio<br>4. Clicar em "Login" | Exibição de mensagem de erro indicando que a senha é obrigatória. |
| LG-006  | Login com conta bloqueada                   | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `locked_out_user`<br>3. Clicar em "Login" | Exibição de mensagem informando que o usuário está bloqueado. |
| LG-007  | Login com falha de desempenho               | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `performance_glitch_user`<br>3. Clicar em "Login" | Exibição de mensagem de sucesso, mas com carregamento acima do tempo esperado. |
| LG-008  | Login com falha de layout                   | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `problem_user`<br>3. Clicar em "Login" | Exibição de erro de layout, como ícones desalinhados ou botões sobrepostos. |
| LG-009  | Login com foco em acessibilidade visual     | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `visual_user`<br>3. Clicar em "Login" | Página inicial deve carregar com elementos visuais acessíveis e ajustados para leitura. |

##### 7.1.1.2 Testes Não Funcionais

| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-NF-001 | Testar login em diferentes navegadores    | 1. Abrir o site no Chrome, Firefox e Edge<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em todos os navegadores testados. |
| LG-NF-002 | Testar tempo de resposta no login         | 1. Inserir credenciais válidas<br>2. Medir o tempo entre o clique em "Login" e o carregamento da página inicial | Tempo de resposta deve ser inferior a 2 segundos. |
| LG-NF-003 | Testar login com múltiplas tentativas simultâneas | 1. Tentar logar simultaneamente em dois dispositivos diferentes<br>2. Verificar comportamento | Sistema deve bloquear uma das sessões ou sincronizar as atividades. |
| LG-NF-004 | Testar login em dispositivos móveis       | 1. Acessar a página de login em um dispositivo móvel<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em dispositivos móveis, com layout ajustado. |

---

### 7.2 API Testing (Restful-Booker)

(Seguir com os cenários existentes...)

---

> **Nota:** Consulte o [Relatório de Resultados](./relatorio-resultados.md) para informações sobre bugs encontrados e sugestões de melhorias.
