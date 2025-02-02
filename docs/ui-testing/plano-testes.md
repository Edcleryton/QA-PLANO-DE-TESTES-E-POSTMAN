# Plano de Testes - Sauce Demo e Restful-Booker

## Índice

1. [Introdução](#introdução)  
2. [Escopo](#escopo)  
3. [Ferramentas de Testes](#ferramentas-de-testes)  
4. [Estratégias de Testes](#estratégias-de-testes)  
5. [Cronograma](#cronograma)  
6. [Tipos de Testes](#tipos-de-testes)  
7. [Cenários de Testes](#cenários-de-testes)  
   - 7.1 [UI Testing (Sauce Demo)](#ui-testing-sauce-demo)  
     - 7.1.1 [Login com diferentes tipos de usuários](#login-com-diferentes-tipos-de-usuarios)  
       - 7.1.1.1 [Testes Funcionais](#testes-funcionais)  
       - 7.1.1.2 [Testes Não Funcionais](#testes-nao-funcionais)  
     - 7.1.2 [Ordenação e filtragem de produtos](#ordenacao-e-filtragem-de-produtos)  
       - 7.1.2.1 [Testes Funcionais](#testes-funcionais-1)  
       - 7.1.2.2 [Testes Não Funcionais](#testes-nao-funcionais-1)  
     - 7.1.3 [Fluxo completo de compra](#fluxo-completo-de-compra)  
       - 7.1.3.1 [Testes Funcionais](#testes-funcionais-2)  
       - 7.1.3.2 [Testes Não Funcionais](#testes-nao-funcionais-2)  
     - 7.1.4 [Remoção de itens do carrinho](#remocao-de-itens-do-carrinho)  
       - 7.1.4.1 [Testes Funcionais](#testes-funcionais-3)  
       - 7.1.4.2 [Testes Não Funcionais](#testes-nao-funcionais-3)  
     - 7.1.5 [Navegação entre páginas](#navegacao-entre-paginas)  
       - 7.1.5.1 [Testes Funcionais](#testes-funcionais-4)  
       - 7.1.5.2 [Testes Não Funcionais](#testes-nao-funcionais-4)  
     - 7.1.6 [Logout](#logout)  
       - 7.1.6.1 [Testes Funcionais](#testes-funcionais-5)  
       - 7.1.6.2 [Testes Não Funcionais](#testes-nao-funcionais-5)  
   - 7.2 [API Testing (Restful-Booker)](#api-testing-restful-booker)  
     - 7.2.1 [Autenticação](#autenticacao)  
     - 7.2.2 [Gestão de reservas](#gestao-de-reservas)  
     - 7.2.3 [Filtros e buscas](#filtros-e-buscas)  

---

## 1. Introdução

Este plano de testes foi desenvolvido para garantir a qualidade das funcionalidades da aplicação Sauce Demo e da API Restful-Booker. Ele cobre testes funcionais e não funcionais, priorizando a experiência do usuário, a acessibilidade e o desempenho.

---

## 2. Escopo

- **UI Testing (Sauce Demo):**
  - Validar os fluxos principais da aplicação: Login com diferentes tipos de usuários disponíveis 
Ordenação e filtragem de produtos, Fluxo completo de compra (do carrinho até finalização), Remoção de itens do carrinho, Navegação entre páginas, Logout.
  - Verificar responsividade e acessibilidade.

- **API Testing (Restful-Booker):**
  - Testar endpoints para autenticação, gestão de reservas e filtros.

---

## 3. Ferramentas de Testes

- **UI Testing:**
  - Google Chrome
  - Lighthouse
  - DevTools

- **API Testing:**
  - Postman
  - Variáveis de ambiente para configuração dinâmica
  - JMeter (para cenários de carga)

- **Controle de Qualidade:**
  - GitHub (armazenamento da estutura do projeto)
  - terabox (armazenamento de evidências)
  - Google Drive (armazenamento de evidências)

---

## 4. Estratégias de Testes

- **Testes Funcionais:** Validação das principais funcionalidades e fluxos críticos.
- **Testes Não Funcionais:** Verificação de acessibilidade, segurança e desempenho.
- **Documentação:** Casos de teste, evidências, e análise de riscos registrados de forma detalhada.

> **Relatório Complementar:** Os resultados dos testes, bugs encontrados e sugestões de melhorias estão documentados no relatório complementar: [Relatório de Resultados](./relatorio-resultados.md).

> **Nota:** As evidências visuais e em vídeo dos testes serão armazenadas externamente para fácil consulta. Acesse através dos links organizados por categoria:

- 🔗 [Evidências de Bugs](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)  
- 🔗 [Evidências de Testes Funcionais](https://terabox.com/s/11J0NPRZJ7hfTIFhCHSMfJA)  
- 🔗 [Evidências de Testes Não Funcionais](https://terabox.com/s/16JvzuwtzvLmdz5cCKArzOw)

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
| LG-001  | Login com credenciais válidas               | 1. Acessar a página de login<br>2. Inserir o usuário `standard_user` e a senha `secret_sauce`<br>3. Clicar em "Login" | Usuário logado com sucesso e redirecionado para a página inicial. |
| LG-002  | Login com credenciais inválidas             | 1. Acessar a página de login<br>2. Inserir o usuário `standard_user` e uma senha inválida<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando falha no login. |
| LG-001  | Login com credenciais válidas               | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `standard_user`<br>3. Clicar em "Login" | Usuário logado com sucesso e redirecionado para a página inicial. |
| LG-002  | Login com credenciais inválidas             | 1. Acessar a página de login<br>2. Inserir email válido e senha inválida<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando falha no login. |
| LG-003  | Login com campos vazios                     | 1. Acessar a página de login<br>2. Deixar os campos "Username" e "Password" vazios<br>3. Clicar em "Login" | Exibição de mensagem de erro solicitando preenchimento dos campos obrigatórios. |
| LG-004  | Login com nome de usuário inexistente       | 1. Acessar a página de login<br>2. Inserir um nome de usuário inexistente (`inexistente_user`) e a senha `secret_sauce`<br>3. Clicar em "Login" | Exibição de mensagem de erro informando que o usuário não existe. |
| LG-005  | Login com senha vazia                       | 1. Acessar a página de login<br>2. Inserir o usuário `standard_user` e deixar o campo de senha vazio<br>3. Clicar em "Login" | Exibição de mensagem de erro indicando que a senha é obrigatória. |
| LG-006  | Login com conta bloqueada                   | 1. Acessar a página de login<br>2. Inserir o usuário `locked_out_user` e a senha `secret_sauce`<br>3. Clicar em "Login" | Exibição de mensagem informando que o usuário está bloqueado. |
| LG-007  | Login com falha de desempenho               | 1. Acessar a página de login<br>2. Inserir o usuário `performance_glitch_user` e a senha `secret_sauce`<br>3. Clicar em "Login"<br>4. Verificar lentidão no carregamento | Exibição de mensagem de sucesso, mas com carregamento acima do tempo esperado. |
| LG-008  | Login com falhas de layout                  | 1. Acessar a página de login<br>2. Verificar a disposição dos campos e botões<br>3. Inserir o usuário `problem_user` e a senha `secret_sauce`<br>4. Clicar em "Login" | Interface deve estar corretamente alinhada e funcional em todos os dispositivos. |
| LG-004  | Login com nome de usuário inexistente       | 1. Acessar a página de login<br>2. Inserir nome de usuário não cadastrado<br>3. Inserir senha válida<br>4. Clicar em "Login" | Exibição de mensagem de erro informando que o usuário não existe. |
| LG-005  | Login com senha vazia                       | 1. Acessar a página de login<br>2. Inserir um nome de usuário válido<br>3. Deixar o campo de senha vazio<br>4. Clicar em "Login" | Exibição de mensagem de erro indicando que a senha é obrigatória. |
| LG-006  | Login com conta bloqueada                   | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `locked_out_user`<br>3. Clicar em "Login" | Exibição de mensagem informando que o usuário está bloqueado. |
| LG-007  | Login com falha de desempenho               | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `performance_glitch_user`<br>3. Clicar em "Login" | Exibição de mensagem de sucesso, mas com carregamento acima do tempo esperado. |
| LG-008  | Login com falha de layout                   | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `problem_user`<br>3. Clicar em "Login" | Exibição de erro de layout, como ícones desalinhados ou botões sobrepostos. |
| LG-009  | Login com foco em acessibilidade visual     | 1. Acessar a página de login<br>2. Inserir credenciais válidas do usuário `visual_user`<br>3. Clicar em "Login" | Página inicial deve carregar com elementos visuais acessíveis e ajustados para leitura. |

---

##### **7.1.1.2 Testes Não Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-NF-001 | Testar login em diferentes navegadores    | 1. Abrir o site no Chrome, Firefox e Edge<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em todos os navegadores testados. |
| LG-NF-002 | Testar tempo de resposta no login         | 1. Inserir credenciais válidas<br>2. Medir o tempo entre o clique em "Login" e o carregamento da página inicial | Tempo de resposta deve ser inferior a 2 segundos. |
| LG-NF-003 | Testar login com múltiplas tentativas simultâneas | 1. Tentar logar simultaneamente em dois dispositivos diferentes<br>2. Verificar comportamento | Sistema deve bloquear uma das sessões ou sincronizar as atividades. |
| LG-NF-004 | Testar login em dispositivos móveis       | 1. Acessar a página de login em um dispositivo móvel<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em dispositivos móveis, com layout ajustado. |

---

#### 7.1.2 Ordenação e filtragem de produtos

##### **7.1.2.1 Testes Funcionais**

| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-001 | Ordenar produtos de A-Z                  | 1. Acessar a página de produtos<br>2. Selecionar "A-Z" no menu de filtros | Produtos exibidos em ordem alfabética crescente. |
| OR-002 | Ordenar produtos de Z-A                  | 1. Acessar a página de produtos<br>2. Selecionar "Z-A" no menu de filtros | Produtos exibidos em ordem alfabética decrescente. |
| OR-003 | Ordenar produtos por preço crescente     | 1. Acessar a página de produtos<br>2. Selecionar "Preço: menor para maior" | Produtos exibidos em ordem crescente de preço. |
| OR-004 | Ordenar produtos por preço decrescente   | 1. Acessar a página de produtos<br>2. Selecionar "Preço: maior para menor" | Produtos exibidos em ordem decrescente de preço. |

---

##### **7.1.2.2 Testes Não Funcionais**

| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-NF-001 | Testar ordenação em dispositivos móveis | 1. Acessar o site no modo "móvel" (DevTools)<br>2. Testar ordenação pelos filtros disponíveis | Ordenação funcional em dispositivos móveis. |
| OR-NF-002 | Verificar tempo de resposta ao aplicar filtros | 1. Selecionar um filtro (ex.: "A-Z") em categorias com muitos produtos<br>2. Medir o tempo para exibição dos resultados | Tempo de carregamento inferior a 2 segundos. |


---

#### 7.1.3 Fluxo completo de compra (do carrinho até finalização)

##### 7.1.3.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| FC-001 | Adicionar produtos ao carrinho               | 1. Acessar a página de produtos<br>2. Selecionar um produto<br>3. Clicar em "Adicionar ao carrinho"             | Produto adicionado com sucesso ao carrinho.   |
| FC-002 | Inserir informações de pagamento             | 1. Realizar checkout<br>2. Preencher informações válidas (nome, endereço, cartão de crédito)<br>3. Confirmar   | Informações processadas corretamente.         |
| FC-003 | Finalizar compra com sucesso                 | 1. Após inserir informações de pagamento válidas<br>2. Clicar em "Finalizar compra"                            | Compra finalizada, página de confirmação exibida. |
| FC-004 | Validar a obrigatoriedade de dados completos no checkout | 1. Acesse o site e adicione produtos ao carrinho.<br>2. Clique no botão "Checkout".<br>3. Preencha apenas "Nome", "Sobrenome" e "Código Postal".<br>4. Clique em "Continuar".<br>5. Tente finalizar a compra. | O sistema deve exibir mensagens de erro para os campos obrigatórios não preenchidos e bloquear a finalização. |


##### 7.1.3.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| FC-NF-001  | Teste de Acessibilidade no Checkout           |  1. Navegar pelo checkout usando apenas o teclado (Tab e Enter).<br>2. Confirmar a funcionalidade de todos os campos e botões. | Todos os elementos devem ser navegáveis, receber foco visível, e realizar as ações esperadas. |
| FC-NF-002  | Testar fluxo de compra em dispositivos móveis  | 1. Realizar uma compra completa no modo "móvel" (DevTools)<br>2. Conferir layout e funcionalidade              | Fluxo funcional e layout responsivo.          |


---

#### 7.1.4 Remoção de itens do carrinho

##### 7.1.4.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| RC-001 | Remover produto individual do carrinho       | 1. Acessar o carrinho com produtos adicionados<br>2. Clicar no botão "Remover" ao lado de um produto            | Produto removido com sucesso.                 |
| RC-002 | Remover todos os produtos do carrinho        | 1. Acessar o carrinho com vários produtos<br>2. Remover os itens um por um até o carrinho ficar vazio           | Carrinho vazio exibido corretamente.          |



##### 7.1.4.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| RC-NF-001  | Verificar acessibilidade na remoção de produtos do carrinho | 1. Navegar pelo carrinho usando apenas o teclado (Tab e Enter). |

---

#### 7.1.5 Navegação entre páginas

##### 7.1.5.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| NP-001 | Navegar para a página inicial                | 1. Clicar no logotipo ou no menu "Home"                                                                        | Redirecionamento para a página inicial.        |
| NP-002 | Navegar para a página de produtos            | 1. Acessar o menu principal<br>2. Clicar na opção "Produtos"                                                   | Página de produtos exibida corretamente.      |
| NP-003 | Navegar para o carrinho                      | 1. Adicionar produtos ao carrinho<br>2. Clicar no ícone ou menu "Carrinho"                                     | Página do carrinho exibida com os itens corretos. |
| NP-004 | Navegar para a página de checkout            | 1. Acessar o carrinho<br>2. Clicar em "Checkout"                                                               | Página de checkout exibida corretamente.       |


##### 7.1.5.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| NP-NF-001  | Verificar responsividade da navegação          | 1. Testar navegação em diferentes tamanhos de tela<br>2. Clicar em links do menu                               | Navegação funcional e layout responsivo.       |
| NP-NF-002  | Verificar comportamento do menu principal    | 1. Navegar pelo menu principal.<br>2. Selecionar todas as opções disponíveis. | Todas as opções do menu devem estar funcionando e redirecionar corretamente. |

---

#### 7.1.6 Logout

##### 7.1.6.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| LO-001 | Realizar logout com sucesso                  | 1. Estar logado<br>2. Clicar em "Logout"                                                                       | Sessão encerrada, redirecionamento para a página de login. |
| LO-002 | Tentar acessar páginas protegidas após logout | 1. Realizar logout<br>2. Tentar acessar qualquer página protegida pelo sistema                                 | Sistema redireciona para a página de login com mensagem de permissão negada. |

##### 7.1.6.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| LO-NF-001  | Verificar tempo de redirecionamento após logout | 1. Realizar logout<br>2. Medir o tempo de redirecionamento para a página de login                              | Redirecionamento realizado em menos de 1 segundo. |
| LO-NF-002  | Testar logout em dispositivos móveis           | 1. Estar logado em um dispositivo móvel<br>2. Realizar logout<br>3. Verificar o redirecionamento                | Logout funcional e redirecionamento correto em dispositivos móveis. |
| LO-NF-003  | Verificar comportamento em múltiplas sessões   | 1. Realizar login em dois dispositivos diferentes<br>2. Efetuar logout em um dispositivo<br>3. Verificar status no outro dispositivo | Sessão é encerrada em ambos os dispositivos. |

---

