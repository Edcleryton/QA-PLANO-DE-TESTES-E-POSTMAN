# Plano de Testes - Sauce Demo

## Índice
1. [Introdução](#introdução)
2. [Arquitetura](#arquitetura)
3. [Ferramentas de Testes](#ferramentas-de-testes)
4. [Estratégias de Testes](#estratégias-de-testes)
5. [Cronograma](#cronograma)
6. [Métricas de Qualidade](#métricas-de-qualidade)
7. [Cenários de Testes](#cenários-de-testes)
8. [Resultados dos Testes](#resultados-dos-testes)
9. [Lista de Bugs Encontrados](#lista-de-bugs-encontrados)
10. [Sugestões de Melhorias](#sugestões-de-melhorias)
11. [Análise de Riscos](#análise-de-riscos)

---

## 1. Introdução

Este plano de teste foi elaborado para validar a funcionalidade e experiência de uso da plataforma Sauce Demo. O objetivo é garantir que os principais fluxos da aplicação estejam funcionando corretamente e proporcionar uma experiência de usuário satisfatória antes do lançamento em produção.

**Objetivos:**
- Validar os fluxos funcionais principais da plataforma.
- Garantir que a interface atenda a critérios de usabilidade e acessibilidade.
- Identificar possíveis problemas que impactem negativamente o negócio ou a experiência do usuário.

**Escopo dos Testes:**
- Login com diferentes tipos de usuários.
- Ordenação e filtragem de produtos.
- Fluxo completo de compra.
- Remoção de itens do carrinho.
- Navegação entre páginas.
- Logout.

---

## 2. Arquitetura

O Sauce Demo é uma aplicação web que simula um e-commerce com foco em testes de funcionalidades de UI e interação com o usuário. A aplicação é acessada diretamente via navegador web e possui uma interface responsiva, adaptando-se a diferentes dispositivos e tamanhos de tela. Não serão feitas suposições sobre o backend ou arquitetura de desenvolvimento, pois a análise está focada nos testes funcionais e de usabilidade.

---

## 3. Ferramentas de Testes

| Tipo de Teste        | Ferramenta             |
|----------------------|------------------------|
| Testes Funcionais    | Navegador Google Chrome |
| Testes de Responsividade | Ferramenta do navegador (DevTools) |
| Teste de Compatibilidade Web | Google Chrome, Edge, Firefox |
| Teste de Usabilidade e Acessibilidade | Ferramenta de inspeção do navegador (DevTools) |

---

## 4. Estratégias de Testes

O plano de testes abrange a validação dos seguintes fluxos:
1. **Login e autenticação**: Verificar o login com diferentes tipos de usuários.
2. **Navegação do site**: Validar a navegação entre as páginas principais, como home, produtos, carrinho e checkout.
3. **Fluxo de compras**: Garantir que o processo de adição, remoção e finalização de compras esteja correto.
4. **Responsividade e Acessibilidade**: Validar o comportamento da aplicação em diferentes dispositivos e tamanhos de tela, além de garantir que a plataforma atenda aos requisitos de acessibilidade.
5. **Acessibilidade**: Avaliar a conformidade da interface com padrões de acessibilidade.
6. **Automação**: Identificar sugestões de automação para fluxos críticos, visando melhorar a eficiência dos testes a longo prazo.

### 4.1 Classificação de Bugs
- **Crítico:** Bugs que impedem o funcionamento de uma funcionalidade principal.
- **Grave:** Afeta parcialmente a funcionalidade, mas o sistema ainda é utilizável.
- **Moderado:** Não afeta o uso principal do sistema, mas pode ser irritante para o usuário.
- **Leve:** Pequenos problemas, como erros de digitação ou falhas estéticas.

---

## 5. Cronograma

| Atividade              | Duração | Data de Início | Data de Término |
|------------------------|---------|----------------|-----------------|
| Planejar Testes        | 1 dia   | 19/11/2024     | 19/11/2024      |
| Projetar Casos de Teste| 1 dia   | 20/11/2024     | 20/11/2024      |
| Implementar Testes     | 2 dias  | 21/11/2024     | 22/11/2024      |
| Executar Testes        | 2 dias  | 23/11/2024     | 24/11/2024      |
| Avaliar Resultados     | 1 dia   | 25/11/2024     | 25/11/2024      |
| Documentar Resultados  | 1 dia   | 26/11/2024     | 26/11/2024      |

---

## 6. Métricas de Qualidade

- **Funcionalidade:** A maioria das funcionalidades deve estar operando conforme o esperado.
- **Links Principais:** Todos os links importantes do site devem estar funcionando corretamente.
- **Taxa de Aceitação:** Nenhum bug classificado como **Crítico** ou **Grave** será aceito em produção.
- **Taxa de Aprovação dos Usuários:** A experiência do usuário deve ser satisfatória em todas as etapas do fluxo de navegação e compras.

---

## 7. Cenários de Testes

### 7.1 UI Testing (Sauce Demo)

#### 7.1.1 Login com diferentes tipos de usuários

##### **Testes Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-001  | Login com credenciais válidas               | 1. Acessar a página de login<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Usuário logado com sucesso.                        |
| LG-002  | Login com credenciais inválidas             | 1. Acessar a página de login<br>2. Inserir email válido e senha inválida<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando falha no login. |
| LG-003  | Login com campos vazios                     | 1. Acessar a página de login<br>2. Deixar os campos "Username" e "Password" vazios<br>3. Clicar em "Login" | Exibição de mensagem de erro solicitando preenchimento dos campos obrigatórios. |
| LG-004  | Login com nome de usuário inválido          | 1. Acessar a página de login<br>2. Inserir um nome de usuário inexistente<br>3. Inserir uma senha válida<br>4. Clicar em "Login" | Exibição de mensagem de erro indicando usuário inválido. |

##### **Testes Não Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-NF-001 | Testar login com teclado apenas           | 1. Usar a tecla "Tab" para navegar pelos campos<br>2. Inserir credenciais<br>3. Pressionar Enter no botão "Login" | Login realizado corretamente com apenas o teclado. |
| LG-NF-002 | Testar login em diferentes navegadores    | 1. Acessar a página em Chrome, Firefox e Edge<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em todos os navegadores testados. |

---

#### 7.1.2 Ordenação e filtragem de produtos

##### **Testes Funcionais**
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-001 | Ordenar produtos por preço               | 1. Acessar a página de produtos<br>2. Selecionar "Ordenar por preço" | Produtos ordenados corretamente        |
| OR-002 | Filtrar produtos por categoria           | 1. Acessar a página de produtos<br>2. Selecionar uma categoria de filtro | Produtos filtrados corretamente        |

##### **Testes Não Funcionais**
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-NF-001 | Testar ordenação em dispositivos móveis | 1. Acessar o site no modo "móvel" (DevTools)<br>2. Testar ordenação por preço | Ordenação funcional em dispositivos móveis. |

---

#### 7.1.3 Fluxo completo de compra (do carrinho até finalização)

##### **Testes Funcionais**
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| FC-001 | Finalizar compra com sucesso             | 1. Acessar o carrinho<br>2. Clicar em "Checkout"<br>3. Preencher informações de pagamento<br>4. Confirmar | Compra finalizada com sucesso          |

---

### 7.2 API Testing (Restful-Booker)

#### 7.2.1 Autenticação

##### **Testes Funcionais**
| ID      | Endpoint               | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|------------------------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| AU-001  | POST /auth             | Gerar token de autenticação                 | 1. Enviar requisição POST com credenciais válidas<br>2. Verificar o retorno da resposta | Token gerado com sucesso.                          |
| AU-002  | POST /auth             | Tentar autenticação com credenciais inválidas | 1. Enviar requisição POST com credenciais inválidas<br>2. Verificar o retorno da resposta | Retorno de erro com código HTTP 401.               |

##### **Testes Não Funcionais**
| ID      | Endpoint               | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|------------------------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| AU-NF-001 | Testar autenticação em carga          | 1. Enviar múltiplas requisições simultâneas ao endpoint POST /auth<br>2. Medir tempo de resposta | Autenticação realizada com tempo de resposta aceitável. |

---

#### 7.2.2 Gestão de Reservas

##### **Testes Funcionais**
| ID      | Endpoint               | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|------------------------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| RB-001  | POST /booking          | Criar nova reserva                          | 1. Enviar requisição POST com dados válidos<br>2. Verificar se a reserva foi criada | Reserva criada com sucesso.                        |
| RB-002  | GET /booking/:id       | Buscar reserva específica                   | 1. Enviar requisição GET com um ID válido<br>2. Verificar os detalhes retornados | Dados da reserva exibidos corretamente.            |

##### **Testes Não Funcionais**
| ID      | Endpoint               | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|------------------------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| RB-NF-001 | Testar carga no endpoint de criação de reservas | 1. Enviar múltiplas requisições POST /booking simultaneamente<br>2. Medir tempo de resposta | Reservas criadas com tempo de resposta aceitável. |
---

## 8. Resultados dos Testes

| Cenário  | Resultado | Observações          |
|----------|-----------|----------------------|
| LG-001   | Aprovado  |                      |
| LG-002   | Aprovado  | Mensagem de erro clara |
| OR-001   | Aprovado  | Ordenação por preço correta |
| FC-001   | Aprovado  | Fluxo de compra completo funcionando |

---

## 9. Lista de Bugs Encontrados

| ID do Bug | Descrição do Bug             | Classificação | Observações |
|-----------|------------------------------|---------------|-------------|
| BUG-001   | Problema de navegação na página de checkout | Grave         | A navegação não funciona corretamente em dispositivos móveis. |
| BUG-002   | Falha na exibição de imagens no carrinho de compras | Moderado      | Imagens de alguns produtos não estão sendo exibidas corretamente no carrinho. |

---

## 10. Sugestões de Melhorias

- Melhorar o contraste de cores dos botões para
