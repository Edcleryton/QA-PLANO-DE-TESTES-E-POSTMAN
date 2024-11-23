# Plano de Testes - Sauce Demo e Restful-Booker

## Índice

1. [Introdução](#introdução)  
2. [Arquitetura](#arquitetura)  
3. [Ferramentas de Testes](#ferramentas-de-testes)  
4. [Estratégias de Testes](#estratégias-de-testes)  
5. [Cronograma](#cronograma)  
6. [Métricas de Qualidade](#métricas-de-qualidade)  
7. [Cenários de Testes](#cenários-de-testes)  
   - 7.1 [UI Testing (Sauce Demo)](#71-ui-testing-sauce-demo)  
     - 7.1.1 [Login com diferentes tipos de usuários](#711-login-com-diferentes-tipos-de-usuarios)  
       - 7.1.1.1 [Testes Funcionais](#7111-testes-funcionais)  
       - 7.1.1.2 [Testes Não Funcionais](#7112-testes-nao-funcionais)  
     - 7.1.2 [Ordenação e filtragem de produtos](#712-ordenacao-e-filtragem-de-produtos)  
       - 7.1.2.1 [Testes Funcionais](#7121-testes-funcionais)  
       - 7.1.2.2 [Testes Não Funcionais](#7122-testes-nao-funcionais)  
     - 7.1.3 [Fluxo completo de compra](#713-fluxo-completo-de-compra)  
       - 7.1.3.1 [Testes Funcionais](#7131-testes-funcionais)  
       - 7.1.3.2 [Testes Não Funcionais](#7132-testes-nao-funcionais)  
     - 7.1.4 [Remoção de itens do carrinho](#714-remocao-de-itens-do-carrinho)  
       - 7.1.4.1 [Testes Funcionais](#7141-testes-funcionais)  
       - 7.1.4.2 [Testes Não Funcionais](#7142-testes-nao-funcionais)  
     - 7.1.5 [Navegação entre páginas](#715-navegacao-entre-paginas)  
       - 7.1.5.1 [Testes Funcionais](#7151-testes-funcionais)  
       - 7.1.5.2 [Testes Não Funcionais](#7152-testes-nao-funcionais)  
     - 7.1.6 [Logout](#716-logout)  
       - 7.1.6.1 [Testes Funcionais](#7161-testes-funcionais)  
       - 7.1.6.2 [Testes Não Funcionais](#7162-testes-nao-funcionais)  
   - 7.2 [API Testing (Restful-Booker)](#72-api-testing-restful-booker)  
     - 7.2.1 [Autenticação](#721-autenticacao)  
       - 7.2.1.1 [Testes Funcionais](#7211-testes-funcionais)  
       - 7.2.1.2 [Testes Não Funcionais](#7212-testes-nao-funcionais)  
     - 7.2.2 [Gestão de reservas](#722-gestao-de-reservas)  
       - 7.2.2.1 [Testes Funcionais](#7221-testes-funcionais)  
       - 7.2.2.2 [Testes Não Funcionais](#7222-testes-nao-funcionais)  
     - 7.2.3 [Filtros e buscas](#723-filtros-e-buscas)  
       - 7.2.3.1 [Testes Funcionais](#7231-testes-funcionais)  
       - 7.2.3.2 [Testes Não Funcionais](#7232-testes-nao-funcionais)  
8. [Resultados dos Testes](#8-resultados-dos-testes)  
9. [Lista de Bugs Encontrados](#9-lista-de-bugs-encontrados)  
10. [Sugestões de Melhorias](#10-sugestoes-de-melhorias)  

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

---

#### **7.1.1.2 Testes Não Funcionais**
| ID      | Descrição                                     | Passos para Reproduzir                                                              | Resultado Esperado                                    |
|---------|---------------------------------------------|-------------------------------------------------------------------------------------|-----------------------------------------------------|
| LG-NF-001 | Testar login em diferentes navegadores    | 1. Abrir o site no Chrome, Firefox e Edge<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em todos os navegadores testados. |
| LG-NF-002 | Testar tempo de resposta no login         | 1. Inserir credenciais válidas<br>2. Medir o tempo entre o clique em "Login" e o carregamento da página inicial | Tempo de resposta deve ser inferior a 2 segundos. |
| LG-NF-003 | Testar login com múltiplas tentativas simultâneas | 1. Tentar logar simultaneamente em dois dispositivos diferentes<br>2. Verificar comportamento | Sistema deve bloquear uma das sessões ou sincronizar as atividades. |
| LG-NF-004 | Testar login em dispositivos móveis       | 1. Acessar a página de login em um dispositivo móvel<br>2. Inserir credenciais válidas<br>3. Clicar em "Login" | Login funcional em dispositivos móveis, com layout ajustado. |

---

#### 7.1.2 Ordenação e filtragem de produtos

##### 7.1.2.1 Testes Funcionais
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-001 | Ordenar produtos por preço crescente     | 1. Acessar a página de produtos<br>2. Selecionar "Preço: menor para maior" | Produtos exibidos em ordem crescente de preço. |
| OR-002 | Ordenar produtos por preço decrescente    | 1. Acessar a página de produtos<br>2. Selecionar "Preço: maior para menor" | Produtos exibidos em ordem decrescente de preço. |
| OR-003 | Filtrar produtos por categoria específica | 1. Acessar a página de produtos<br>2. Selecionar uma categoria de filtro (ex.: Eletrônicos) | Apenas produtos da categoria selecionada são exibidos. |
| OR-004 | Filtrar produtos por múltiplos critérios  | 1. Aplicar mais de um filtro (ex.: categoria e preço)<br>2. Verificar os produtos exibidos | Produtos correspondentes a todos os critérios aplicados são exibidos. |

##### 7.1.2.2 Testes Não Funcionais
| ID     | Descrição                                  | Passos para Reproduzir                   | Resultado Esperado                      |
|--------|------------------------------------------|------------------------------------------|-----------------------------------------|
| OR-NF-001 | Testar ordenação em dispositivos móveis | 1. Acessar o site no modo "móvel" (DevTools)<br>2. Testar ordenação por preço | Ordenação funcional em dispositivos móveis. |
| OR-NF-002 | Verificar tempo de carregamento após filtros | 1. Aplicar filtros em categorias com muitos produtos<br>2. Medir o tempo para exibição dos resultados | Tempo de carregamento inferior a 2 segundos. |
| OR-NF-003 | Verificar comportamento com categorias vazias | 1. Aplicar filtro para uma categoria sem produtos<br>2. Conferir mensagem exibida | Mensagem clara informando que não há produtos disponíveis. |

---

#### 7.1.3 Fluxo completo de compra (do carrinho até finalização)

##### 7.1.3.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| FC-001 | Adicionar produtos ao carrinho               | 1. Acessar a página de produtos<br>2. Selecionar um produto<br>3. Clicar em "Adicionar ao carrinho"             | Produto adicionado com sucesso ao carrinho.   |
| FC-002 | Inserir informações de pagamento             | 1. Realizar checkout<br>2. Preencher informações válidas (nome, endereço, cartão de crédito)<br>3. Confirmar   | Informações processadas corretamente.         |
| FC-003 | Finalizar compra com sucesso                 | 1. Após inserir informações de pagamento válidas<br>2. Clicar em "Finalizar compra"                            | Compra finalizada, página de confirmação exibida. |
| FC-004 | Não finalizar compra com informações inválidas | 1. Realizar checkout<br>2. Preencher informações inválidas (ex.: número de cartão incorreto)<br>3. Confirmar   | Exibição de mensagem de erro indicando problema nas informações inseridas. |
| FC-005 | Verificar comportamento com produtos fora de estoque | 1. Adicionar produto ao carrinho<br>2. Realizar checkout<br>3. Produto fica fora de estoque no processo | Mensagem informando indisponibilidade do produto. |

##### 7.1.3.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| FC-NF-001  | Verificar tempo de resposta no checkout        | 1. Realizar checkout<br>2. Medir o tempo entre o clique em "Finalizar compra" e o carregamento da página final | Tempo de resposta inferior a 3 segundos.      |
| FC-NF-002  | Testar fluxo de compra em dispositivos móveis  | 1. Realizar uma compra completa no modo "móvel" (DevTools)<br>2. Conferir layout e funcionalidade              | Fluxo funcional e layout responsivo.          |
| FC-NF-003  | Verificar comportamento com alta carga de usuários | 1. Simular múltiplos acessos simultâneos ao checkout<br>2. Realizar compras paralelas                          | Sistema mantém desempenho estável sem falhas. |

---

#### 7.1.4 Remoção de itens do carrinho

##### 7.1.4.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| RC-001 | Remover produto individual do carrinho       | 1. Acessar o carrinho com produtos adicionados<br>2. Clicar no botão "Remover" ao lado de um produto            | Produto removido com sucesso.                 |
| RC-002 | Remover todos os produtos do carrinho        | 1. Acessar o carrinho com vários produtos<br>2. Remover os itens um por um até o carrinho ficar vazio           | Carrinho vazio exibido corretamente.          |
| RC-003 | Exibir mensagem ao tentar remover produto inexistente | 1. Acessar o carrinho<br>2. Tentar remover um produto que já foi removido anteriormente                        | Mensagem de erro ou aviso indicando item inexistente. |

##### 7.1.4.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| RC-NF-001  | Verificar tempo de resposta ao remover produtos | 1. Remover produtos do carrinho repetidamente<br>2. Medir o tempo de resposta após cada ação                   | Tempo de resposta inferior a 1 segundo.       |
| RC-NF-002  | Verificar comportamento ao remover produtos com baixa conectividade | 1. Simular ambiente de internet lenta ou instável<br>2. Remover produto do carrinho                           | Produto removido com sucesso, com notificações de status exibidas. |

---

#### 7.1.5 Navegação entre páginas

##### 7.1.5.1 Testes Funcionais
| ID     | Descrição                                      | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|--------|----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| NP-001 | Navegar para a página inicial                | 1. Clicar no logotipo ou no menu "Home"                                                                        | Redirecionamento para a página inicial.        |
| NP-002 | Navegar para a página de produtos            | 1. Acessar o menu principal<br>2. Clicar na opção "Produtos"                                                   | Página de produtos exibida corretamente.      |
| NP-003 | Navegar para o carrinho                      | 1. Adicionar produtos ao carrinho<br>2. Clicar no ícone ou menu "Carrinho"                                     | Página do carrinho exibida com os itens corretos. |
| NP-004 | Navegar para a página de checkout            | 1. Acessar o carrinho<br>2. Clicar em "Checkout"                                                               | Página de checkout exibida corretamente.       |
| NP-005 | Navegar para uma página inexistente          | 1. Digitar uma URL inválida ou inexistente<br>2. Pressionar Enter                                              | Sistema exibe página de erro 404 com navegação de retorno. |

##### 7.1.5.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                           | Resultado Esperado                              |
|------------|-----------------------------------------------|----------------------------------------------------------------------------------------------------------------|-----------------------------------------------|
| NP-NF-001  | Verificar responsividade da navegação          | 1. Testar navegação em diferentes tamanhos de tela<br>2. Clicar em links do menu                               | Navegação funcional e layout responsivo.       |
| NP-NF-002  | Testar tempo de carregamento ao navegar        | 1. Navegar entre páginas principais<br>2. Medir tempo de carregamento em cada transição                        | Tempo de carregamento inferior a 2 segundos.   |
| NP-NF-003  | Testar navegação com links quebrados           | 1. Identificar links desatualizados ou inexistentes no menu<br>2. Tentar acessá-los                            | Sistema exibe mensagem clara de erro ou redireciona para a página inicial. |

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

### 7.2 API Testing (Restful-Booker)

#### 7.2.1 Autenticação

##### 7.2.1.1 Testes Funcionais
| ID      | Descrição                                   | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|---------|-------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| AU-001  | Gerar token com credenciais válidas       | 1. Realizar uma requisição POST no endpoint `/auth`<br>2. Enviar credenciais válidas no corpo da requisição | Token de autenticação gerado com sucesso, retornando código 200.          |
| AU-002  | Tentar gerar token com credenciais inválidas | 1. Realizar uma requisição POST no endpoint `/auth`<br>2. Enviar credenciais inválidas no corpo da requisição | Resposta com código 401 e mensagem de erro indicando "Credenciais inválidas".         |

##### 7.2.1.2 Testes Não Funcionais
| ID         | Descrição                                      | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|------------|----------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| AU-NF-001  | Verificar tempo de resposta na autenticação   | 1. Realizar uma requisição POST no endpoint `/auth` com credenciais válidas<br>2. Medir o tempo de resposta | Tempo de resposta inferior a 2 segundos.           |
| AU-NF-002  | Testar autenticação com múltiplas requisições simultâneas | 1. Enviar 10 requisições simultâneas ao endpoint `/auth` com credenciais válidas                      | Todas as requisições retornam tokens válidos, sem falhas. |

---

#### 7.2.2 Gestão de reservas

##### 7.2.2.1 Testes Funcionais
| ID      | Descrição                                   | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|---------|-------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| GR-001  | Criar uma nova reserva                    | 1. Realizar uma requisição POST no endpoint `/booking`<br>2. Enviar dados válidos no corpo da requisição | Reserva criada com sucesso, retornando ID da reserva e código 200. |
| GR-002  | Buscar uma reserva específica             | 1. Realizar uma requisição GET no endpoint `/booking/{id}`<br>2. Informar um ID válido na URL           | Detalhes da reserva retornados corretamente, com código 200.        |
| GR-003  | Listar todas as reservas                  | 1. Realizar uma requisição GET no endpoint `/booking`                                                 | Lista de reservas retornada corretamente, com código 200.          |
| GR-004  | Atualizar uma reserva existente           | 1. Realizar uma requisição PUT no endpoint `/booking/{id}`<br>2. Enviar novos dados no corpo da requisição | Reserva atualizada com sucesso, retornando código 200.              |
| GR-005  | Deletar uma reserva existente             | 1. Realizar uma requisição DELETE no endpoint `/booking/{id}`<br>2. Informar um ID válido na URL       | Reserva deletada com sucesso, retornando código 201.                |
| GR-006  | Buscar reserva inexistente                | 1. Realizar uma requisição GET no endpoint `/booking/{id}`<br>2. Informar um ID inválido na URL         | Resposta com código 404 e mensagem de erro indicando que a reserva não existe. |

##### 7.2.2.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| GR-NF-001  | Verificar tempo de resposta ao criar reservas  | 1. Realizar uma requisição POST no endpoint `/booking` com dados válidos<br>2. Medir o tempo de resposta | Tempo de resposta inferior a 3 segundos.           |
| GR-NF-002  | Testar comportamento com alta carga de reservas | 1. Criar múltiplas reservas simultaneamente (ex.: 50 requisições)<br>2. Monitorar respostas do servidor | Todas as requisições processadas corretamente, sem quedas de desempenho.      |

---

#### 7.2.3 Filtros e buscas

##### 7.2.3.1 Testes Funcionais
| ID      | Descrição                                   | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|---------|-------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| FB-001  | Buscar reservas por nome                  | 1. Realizar uma requisição GET no endpoint `/booking?firstname={nome}`<br>2. Informar um nome válido na query | Reservas correspondentes ao nome retornadas corretamente, com código 200.        |
| FB-002  | Buscar reservas por data de check-in      | 1. Realizar uma requisição GET no endpoint `/booking?checkin={data}`<br>2. Informar uma data válida na query | Reservas com a data de check-in correspondente retornadas corretamente. |
| FB-003  | Buscar reservas por data de check-out     | 1. Realizar uma requisição GET no endpoint `/booking?checkout={data}`<br>2. Informar uma data válida na query | Reservas com a data de check-out correspondente retornadas corretamente. |
| FB-004  | Buscar reservas com múltiplos filtros     | 1. Realizar uma requisição GET no endpoint `/booking` com múltiplos parâmetros (ex.: `firstname` e `checkin`) | Reservas que atendem a todos os filtros retornadas corretamente, com código 200. |

##### 7.2.3.2 Testes Não Funcionais
| ID         | Descrição                                       | Passos para Reproduzir                                                                                 | Resultado Esperado                                    |
|------------|-----------------------------------------------|--------------------------------------------------------------------------------------------------------|-----------------------------------------------------|
| FB-NF-001  | Verificar tempo de resposta em buscas com filtros | 1. Realizar requisições GET com diferentes combinações de filtros<br>2. Medir o tempo de resposta      | Tempo de resposta inferior a 2 segundos.           |
| FB-NF-002  | Testar comportamento ao aplicar filtros inválidos | 1. Realizar requisições GET com parâmetros inválidos (ex.: `checkin=invalid-date`)<br>2. Verificar respostas | Resposta com código 400 e mensagem de erro clara.   |
| FB-NF-003  | Testar busca em grandes volumes de dados        | 1. Aplicar filtros em uma base de dados com mais de 10.000 registros<br>2. Monitorar o desempenho      | Resultados retornados sem impacto significativo no desempenho. |


---

## 8. Resultados dos Testes

| Cenário  | Resultado | Observações          |
|----------|-----------|----------------------|
| LG-001   | Aprovado  | Login com credenciais válidas funcionando como esperado. |
| LG-002   | Aprovado  | Mensagem de erro clara para login inválido. |
| LG-003   | Aprovado  | Mensagem de erro exibida corretamente para campos vazios. |
| OR-001   | Aprovado  | Ordenação por preço (menor para maior) funcionando corretamente. |
| OR-002   | Aprovado  | Ordenação por preço (maior para menor) funcional. |
| OR-003   | Aprovado  | Filtro por categoria retorna resultados consistentes. |
| FC-001   | Aprovado  | Produto adicionado ao carrinho com sucesso. |
| FC-002   | Aprovado  | Fluxo de compra completo funcionando, sem erros. |
| RC-001   | Aprovado  | Remoção de produto individual do carrinho realizada com sucesso. |
| NP-001   | Aprovado  | Navegação entre páginas principais fluida e funcional. |
| LO-001   | Aprovado  | Logout executado com sucesso, redirecionando corretamente para a página de login. |

---

## 9. Lista de Bugs Encontrados

| ID do Bug | Descrição do Bug                          | Classificação | Observações                                               |
|-----------|------------------------------------------|---------------|----------------------------------------------------------|
| BUG-001   | Problema de navegação na página de checkout | Grave         | A navegação não funciona corretamente em dispositivos móveis. |
| BUG-002   | Falha na exibição de imagens no carrinho de compras | Moderado      | Imagens de alguns produtos não estão sendo exibidas corretamente no carrinho. |
| BUG-003   | Mensagem de erro genérica para login com senha inválida | Leve          | A mensagem não informa se o problema é no nome de usuário ou na senha. |
| BUG-004   | Tempo elevado ao aplicar múltiplos filtros simultâneos | Moderado      | O tempo de resposta excede 5 segundos quando muitos filtros são aplicados. |
| BUG-005   | Botão "Logout" às vezes não responde em dispositivos móveis | Grave         | O botão exige múltiplos cliques para funcionar. |

---

## 10. Sugestões de Melhorias

1. **Interface do Usuário (UI):**
   - **Contraste de cores:** Aumentar o contraste de cores dos botões para melhorar a acessibilidade e a visibilidade.
   - **Redimensionamento de imagens:** Garantir que todas as imagens do carrinho sejam carregadas e ajustadas ao tamanho ideal.
   - **Erros detalhados:** Exibir mensagens de erro mais informativas no login para ajudar os usuários a corrigirem os problemas rapidamente.

2. **Experiência do Usuário (UX):**
   - **Feedback visual:** Adicionar feedback visual (ex.: loaders ou spinners) em ações como filtros e checkout.
   - **Melhoria no fluxo de logout:** Resolver o problema de resposta do botão "Logout" em dispositivos móveis.
   - **Filtros otimizados:** Melhorar o desempenho ao aplicar múltiplos filtros simultaneamente.

3. **Performance:**
   - **Tempo de resposta:** Garantir que todas as ações, como navegação e aplicação de filtros, tenham tempo de resposta inferior a 2 segundos.
   - **Teste de carga:** Simular cenários com alta carga de usuários para garantir estabilidade durante picos de acesso.

4. **Acessibilidade:**
   - **Teclado:** Permitir navegação completa utilizando apenas o teclado (Tab/Enter).
   - **Textos alternativos:** Adicionar textos alternativos (alt) em imagens para suporte a leitores de tela.
   - **Responsividade:** Garantir que todos os elementos sejam funcionais e visíveis em diferentes tamanhos de tela.

5. **Automação:**
   - Sugerir a automação dos testes críticos, como login, fluxo de compra e filtros, para aumentar a eficiência e a cobertura dos testes futuros.
