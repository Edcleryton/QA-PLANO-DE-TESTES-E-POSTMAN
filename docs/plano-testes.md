# Plano de Testes - Sauce Demo

## Índice

## Índice
1. [Introdução](#introdução)
2. [Arquitetura](#arquitetura)
3. [Ferramentas de Testes](#ferramentas-de-testes)
4. [Estratégias de Testes](#estratégias-de-testes)
5. [Cronograma](#cronograma)
6. [Métricas de Qualidade](#métricas-de-qualidade)
7. [Cenários de Testes](#cenários-de-testes)
8. [Resultados dos Testes](#resultados-dos-testes)
9. [Sugestões de Melhorias](#sugestões-de-melhorias)
10. [Análise de Riscos](#análise-de-riscos)


## 1. Introdução
Este plano de teste descreve a abordagem para verificar a funcionalidade do e-commerce Sauce Demo. O objetivo é validar os principais fluxos do sistema antes do lançamento em produção.

**Ambiente de teste:** https://www.saucedemo.com

### 1.1 Objetivo
Validar a funcionalidade e usabilidade da plataforma Sauce Demo, garantindo a qualidade do software através de testes manuais dos principais fluxos da aplicação.

### 1.2 Escopo
- Login com diferentes tipos de usuários
- Ordenação e filtragem de produtos
- Fluxo completo de compra
- Gerenciamento do carrinho
- Navegação entre páginas
- Logout

### 1.3 Fora do Escopo
- Testes de API
- Testes de carga
- Testes de segurança

## 2. Arquitetura
O sistema do site Sauce Demo é uma aplicação monolítica construída em Python, que integra o backend com um frontend desenvolvido utilizando HTML, CSS e JavaScript. Toda a estrutura foi projetada para ser robusta e eficiente, garantindo que as funcionalidades principais sejam processadas de forma integrada dentro desse monólito. O Sauce Demo é uma aplicação web demonstrativa que simula um e-commerce, construída para fins de teste, com:

- Frontend: HTML, CSS, JavaScript
- Stack moderna de desenvolvimento web
- Interface responsiva
- Simulação de diferentes estados de usuário e comportamentos

A hospedagem é feita na AWS (Amazon Web Services), utilizando os serviços de computação em nuvem, o que oferece escalabilidade e alta disponibilidade. Esse ambiente permite que o sistema tenha um bom desempenho e segurança, além de facilitar o gerenciamento e a manutenção do projeto ao longo do tempo.

## 3. Ferramentas de Testes
Serão utilizadas as seguintes ferramentas para testes do Sauce Demo:

| Tipo de Teste | Ferramenta |
| --- | --- |
| Testes UI | Computador com Windows 10 ou 11, Navegadores Web (Google Chrome), Chrome DevTools, LightHouse |
| Teste de Compatibilidade Web | Computador com Windows 10 ou 11, Navegadores Web (Google Chrome, Edge, Firefox) |
| Teste de Funcionalidade Web | Execução manual utilizando o navegador Google Chrome e inspeção via DevTools (Google Chrome Developer Tools) |
| Teste de Performance Web | Google Lighthouse (ferramenta para medir performance de websites) executado no Google Chrome |

**Nota:** O Google Lighthouse será utilizado para avaliar a qualidade geral da aplicação web, verificando as métricas de desempenho, acessibilidade, práticas recomendadas e SEO. Essas métricas ajudarão a identificar melhorias técnicas e de usabilidade.

## 4. Estratégias de Testes
O escopo dos testes abrange a validação das seguintes funcionalidades principais do Sauce Demo:

1. **Navegação do site:** validação da navegação entre as principais páginas (home, produtos, carrinho, pagamento);
2. **Criação de conta:** testar o fluxo de registro de novos usuários;
3. **Fluxo de compras:** verificar a adição e remoção de itens do carrinho;
4. **Processo de pagamento:** garantir que o pagamento seja processado corretamente.

Além disso, serão realizados:

- **Testes de Qualidade e Desempenho:** a aplicação será testada em quatro métricas (Performance, Acessibilidade, Práticas Recomendadas e SEO), utilizando o Google Lighthouse. Isso assegura que o site atenda a padrões de qualidade que impactam a experiência do usuário e a eficiência do sistema.
- **Testes Manuais:** serão executados pela equipe de QA's. Todos os casos de testes descritos no cenário de testes deverão ser executados e passar sem maiores problemas.

### 4.1 Classificação dos Bugs
- **Critical/Blocker:** bugs que não permitem o pleno funcionamento de requisitos funcionais. Sendo impraticável, ir para produção.
- **Grave:** bugs que afetam parcialmente o funcionamento da funcionalidade, impedindo que ela opere plenamente, mas sem comprometer seu funcionamento básico.
- **Moderada:** bugs que não atrapalham a funcionalidade do serviço.
- **Leve:** pequenos erros visuais ou ortográficos.

## 5. Cronograma
| Atividade | Duração | Data de Início | Data de Término |
| --- | --- | --- | --- |
| Planejar Testes | 3 dias | 16/11/2024 | 18/11/2024 |
| Projetar Casos de Testes | 4 dias | 19/11/2024 | 22/11/2024 |
| Implementar Testes | 3 dias | 23/11/2024 | 24/11/2024 |
| Executar Testes | 4 dias | 26/11/2024 | 29/11/2024 |
| Avaliar Resultados | 1 dia | 30/11/2024 | 30/11/2024 |

## 6. Métricas de Qualidade
**Métricas para Lançamento do Site:**
- **Funcionalidade:** a maioria das funcionalidades do site deve estar operando conforme o esperado;
- **Links Principais:** todos os links de acesso importantes não devem apresentar erros de indexação;
- **Formulário de Contato:** deve estar completamente funcional.

**Taxa de Aceitação:** não serão aceitos bugs classificados como Blocker/Critical ou Grave no ambiente de produção.

**Taxa de Aprovação dos Usuários:** para o lançamento, todos os usuários da versão em homologação devem relatar uma experiência satisfatória.

**Tempo de Resposta para Correção dos Bugs:** Blocker e Grave: devem ser corrigidos em até 3 dias.

## 7. Cenários de Testes
### 7.1 Fluxo de Navegação do Usuário
| ID | Objetivo | Passo a Passo | Resultado Esperado |
| --- | --- | --- | --- |
| NAV-001 | Verificar a navegação pelo menu principal | 1. Acessar a página inicial<br>2. Clicar no menu "Home"| O usuário deve ser redirecionado corretamente para a página inicial |
| NAV-002 | Validar o redirecionamento ao clicar no logotipo | 1. Acessar qualquer página<br>2. Clicar no logotipo do site | O usuário deve ser redirecionado para a página inicial |
| NAV-003 | Testar a navegação entre categorias e o filtro por categoria | 1. Acessar a página de categorias<br>2. Clicar em uma categoria | O site deve direcionar corretamente para a página da categoria selecionada e exibir os produtos correspondentes |
| ... | ... | ... | ... |

### 7.2 Fluxo de Criação de Conta
| ID | Objetivo | Passo a Passo | Resultado Esperado |
| --- | --- | --- | --- |
| CC-001 | Criar conta de usuário com sucesso | 1. Acessar a página de registro<br>2. Preencher todos os campos obrigatórios<br>3. Clicar em "Registrar" | A conta deve ser criada com sucesso e o usuário redirecionado para a página de boas-vindas |
| CC-002 | Tentar criar conta com campos obrigatórios vazios | 1. Acessar a página de registro<br>2. Deixar campos obrigatórios em branco<br>3. Clicar em "Registrar" | O sistema deve exibir uma mensagem de erro solicitando o preenchimento dos campos obrigatórios |
| ... | ... | ... | ... |

### 7.3 Fluxo de Compra e Carrinho
| ID | Objetivo | Passo a Passo | Resultado Esperado |
| --- | --- | --- | --- |
| CRC-001 | Adicionar itens ao carrinho | 1. Acessar a página de produtos<br>2. Clicar em "Adicionar ao carrinho" | O carrinho deve ser atualizado corretamente com os itens selecionados |
| CRC-002 | Remover itens do carrinho | 1. Acessar a página do carrinho<br>2. Clicar em "Remover" | O item deve ser removido corretamente do carrinho |
| ... | ... | ... | ... |

### 7.4 Fluxo de Pagamento
| ID | Objetivo | Passo a Passo | Resultado Esperado |
| --- | --- | --- | --- |
| PG-001 | Processar pagamento com sucesso | 1. Acessar a página de pagamento<br>2. Preencher as informações de pagamento<br>3. Clicar em "Finalizar" | O pagamento deve ser processado com sucesso, sem erros, e o usuário redirecionado para a página de confirmação |
| PG-002 | Falha no pagamento com cartão inválido | 1. Acessar a página de pagamento<br>2. Inserir um cartão de crédito inválido<br>3. Tentar processar o pagamento | O sistema deve exibir uma mensagem de erro informando que o pagamento foi recusado |
| ... | ... | ... | ... |

## 8. Resultados dos Testes
[Aqui serão adicionados os resultados dos testes executados, incluindo capturas de tela relevantes.]

## 9. Sugestões de Melhorias
[Aqui serão adicionadas as sugestões de melhorias de UX/UI identificadas durante os testes.]

## 10. Análise de Riscos
[Aqui serão adicionados os principais riscos identificados e suas possíveis mitigações.]
