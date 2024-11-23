# Teste Prático QA 🛠️

Este repositório contém a documentação e as evidências dos testes realizados para o desafio QA Testing BeTalent. Os testes estão divididos em dois tipos principais: **UI Testing** e **API Testing**.

---

## 📌 Status do Projeto
✅ Em andamento

---

## 📌 Índice
1. [Descrição do Projeto](#descrição-do-projeto)  
2. [Estrutura do Repositório](#estrutura-do-repositório)  
3. [Testes Realizados](#testes-realizados)  
   - [UI Testing (Sauce Demo)](#ui-testing-sauce-demo)  
   - [API Testing (Restful-Booker)](#api-testing-restful-booker)  
4. [Como Reproduzir os Testes](#como-reproduzir-os-testes)  
5. [Ferramentas Utilizadas](#ferramentas-utilizadas)  
6. [Colaborador](#colaborador)  

---

## 📌 Descrição do Projeto

O objetivo deste projeto é validar as funcionalidades da aplicação **Sauce Demo** e da API **Restful-Booker**. Ele inclui testes funcionais e não funcionais, priorizando a experiência do usuário, desempenho e acessibilidade.  

Os testes foram planejados com base em critérios de aceitação funcionais e não funcionais, garantindo qualidade nas entregas.

**Objetivos principais:**
- Validar fluxos de login, navegação e ações principais da interface gráfica (UI Testing).
- Testar endpoints para autenticação, gestão de reservas e buscas (API Testing).

---

## 📌 Estrutura do Repositório

A organização do repositório é a seguinte:

- **`README.md`**: Este arquivo, contendo informações gerais do projeto.
- **`docs/`**:  
  - **`plano-testes.md`**: Documento com os planos de testes detalhados.  
  - **`relatorio-resultados.md`**: Documento complementar com os resultados dos testes, bugs encontrados e sugestões de melhorias.

---

## 📌 Testes Realizados

### **1. UI Testing (Sauce Demo)**

#### **Objetivo**
Validar os principais fluxos de funcionalidade e usabilidade da aplicação Sauce Demo para garantir a experiência do usuário.

#### **Cenários Testados**
1. Login com diferentes tipos de usuários disponíveis.
2. Ordenação e filtragem de produtos.
3. Fluxo completo de compra (do carrinho até finalização).
4. Remoção de itens do carrinho.
5. Navegação entre páginas.
6. Logout.

#### **Evidências**
As evidências relacionadas aos testes estão disponíveis no Terabox.  
- 🔗 [Evidências de Bugs e Testes](https://terabox.com/s/10G4Pl6pXZg24-Cvs2eCMvA)

---

### **2. API Testing (Restful-Booker)**

#### **Objetivo**
Garantir que os principais endpoints da API Restful-Booker estejam funcionando corretamente.

#### **Cenários Testados**
1. **Autenticação**:
   - Gerar token de autenticação.
   - Testar autenticação com credenciais inválidas.
2. **Gestão de Reservas**:
   - Criar, buscar, atualizar, listar e deletar reservas.
3. **Filtros e Buscas**:
   - Buscar reservas por nome, data de check-in e check-out.

#### **Evidências**
As evidências dos testes de API estão disponíveis no Terabox.  
- 🔗 [Evidências de API](https://terabox.com/s/1Tt3Bz1a6JdNAH-dLprAJcQ)

---

## 📌 Como Reproduzir os Testes

### **UI Testing**
1. Acesse a aplicação Sauce Demo: [https://www.saucedemo.com](https://www.saucedemo.com).
2. Consulte o documento `docs/plano-testes.md` para os passos detalhados de cada cenário.

### **API Testing**
1. Importe a collection do Postman disponível na pasta `docs/`.
2. Configure as variáveis de ambiente incluídas na collection.
3. Consulte o documento `docs/plano-testes.md` para os passos detalhados de cada cenário.

---

## 📌 Ferramentas Utilizadas 💻

- **UI Testing**:
  - Navegadores: Google Chrome, Edge.
  - Lighthouse: Para verificar acessibilidade e desempenho.
  - DevTools: Para inspeção e validação de tempos de resposta.

- **API Testing**:
  - **Postman**: Criação e execução de requisições de teste.

---

## 📌 Colaborador ✨

- **Edcleryton Gabriel**: Autor e responsável pelos testes.

---

**Contato**  

E-mail: [edcleryton.gabriel@gmail.com](mailto:edcleryton.gabriel@gmail.com)  
LinkedIn: [Edcleryton Silva](https://www.linkedin.com/in/edcleryton-silva/)  
GitHub: [Edcleryton](https://github.com/Edcleryton)  
Whatsapp: +55 (71) 9 9386-5329

---

> **Nota:** Consulte os documentos `docs/plano-testes.md` e `docs/relatorio-resultados.md` para mais detalhes sobre o planejamento e os resultados dos testes.

**Vamos garantir a qualidade! 🚀**
