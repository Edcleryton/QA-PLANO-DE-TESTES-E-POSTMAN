# Plano de Testes - Sauce Demo e Restful-Booker

## Índice
1. [Introdução](#introdução)
2. [Escopo](#escopo)
3. [Ferramentas Utilizadas](#ferramentas-utilizadas)
4. [Estratégias de Testes](#estratégias-de-testes)
5. [Cronograma](#cronograma)
6. [Tipos de Testes](#tipos-de-testes)
7. [Cenários de Testes](#cenários-de-testes)
   - [7.1 UI Testing (Sauce Demo)](#71-ui-testing-sauce-demo)
   - [7.2 API Testing (Restful-Booker)](#72-api-testing-restful-booker)
8. [Resultados dos Testes](#resultados-dos-testes)
9. [Lista de Bugs Encontrados](#lista-de-bugs-encontrados)
10. [Sugestões de Melhorias](#sugestões-de-melhorias)
11. [Análise de Riscos](#análise-de-riscos)

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

## 3. Ferramentas Utilizadas

- **UI Testing:** Google Chrome, Firefox, Lighthouse, DevTools.
- **API Testing:** Postman, variáveis de ambiente para configuração dinâmica.

---

## 4. Estratégias de Testes

- **Testes Funcionais:** Validação das principais funcionalidades e fluxos críticos.
- **Testes Não Funcionais:** Verificação de acessibilidade, segurança e desempenho.
- **Documentação:** Registros detalhados dos resultados, com evidências e análise de riscos.

---

## 5. Cronograma

| Atividade              | Duração | Data de Início | Data de Término |
|------------------------|---------|----------------|-----------------|
| Planejar Testes        | 1 dia   | 19/11/2024     | 19/11/2024      |
| Criar Casos de Teste   | 2 dias  | 20/11/2024     | 21/11/2024      |
| Executar Testes (UI)   | 2 dias  | 22/11/2024     | 23/11/2024      |
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

##### **Testes Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-001  | Login com credenciais válidas               | 1. Acessar a página de login<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Usuário logado com sucesso.                        |
| LG-002  | Login com credenciais inválidas             | 1. Acessar a página de login<br>2. Inserir email válido e senha inválida<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando falha no login. |

##### **Testes Não Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-NF-001 | Testar login em diferentes navegadores    | 1. Abrir o site no Chrome, Firefox e Edge<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em todos os navegadores testados. |

---

#### 7.1.2 Ordenação e filtragem de produtos

##### **Testes Funcionais**
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-001 | Ordenar produtos por preço               | 1. Acessar a página de produtos<br>2. Selecionar "Ordenar por preço" | Produtos ordenados corretamente        |

---

### 7.2 API Testing (Restful-Booker)

#### 7.2.1 Autenticação

##### **Testes Funcionais**
| ID      | Endpoint               | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|------------------------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| AU-001  | POST /auth             | Gerar token de autenticação                 | 1. Enviar requisição POST com credenciais válidas<br>2. Verificar o retorno da resposta | Token gerado com sucesso.                          |

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
