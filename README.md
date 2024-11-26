
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
- 🔗 [Evidências de Bugs e Testes de UI](https://terabox.com/s/1H1Sfa4v3n23hNK3Buxj6YA)

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
Os testes de API podem ser importados diretamente para o Postman usando o arquivo JSON disponível neste repositório.  

- 🔗 **[Download da Collection JSON](./docs/api-testing/api-testing-collection.json)**  
- 🔗 [Documentação dos Testes de API](./docs/api-testing/plano-testes.md)

**Como Importar para o Postman**:
1. Faça o download do arquivo `api-testing-collection.json`.
2. No Postman, clique em **Import** (ícone de seta no canto superior esquerdo).
3. Selecione o arquivo baixado e importe a coleção.

---

## 📌 Como Reproduzir os Testes

### **UI Testing**
1. Acesse a aplicação Sauce Demo: [https://www.saucedemo.com](https://www.saucedemo.com).
2. Consulte o documento `docs/ui-testing/plano-testes.md` para os passos detalhados de cada cenário.

### **API Testing**
1. Importe a collection do Postman disponível na pasta `docs/api-testing/`.
2. Configure as variáveis de ambiente incluídas na collection.
3. Consulte o documento `docs/api-testing/plano-testes.md` para os passos detalhados de cada cenário.

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

---

> **Nota:** Consulte os documentos `docs/ui-testing/plano-testes.md`, `docs/api-testing/plano-testes.md` e `docs/ui-testing/relatorio-resultados.md` para mais detalhes sobre o planejamento e os resultados dos testes.

**Vamos garantir a qualidade! 🚀**
