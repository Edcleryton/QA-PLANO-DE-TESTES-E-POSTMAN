# 📌 Testes Realizados

Este repositório abrange **UI Testing** (Sauce Demo) e **API Testing** (Restful Booker), seguindo os requisitos propostos no desafio. Todas as instruções de planejamento, execução e resultados foram documentadas em arquivos Markdown dentro da pasta `docs/`.

---

## 1. UI Testing (Sauce Demo)

**Objetivo:**  
Validar os principais fluxos de funcionalidade e usabilidade da aplicação [Sauce Demo](https://www.saucedemo.com) para garantir a experiência do usuário antes do lançamento em produção.

**Cenários Testados:**
- Login com diferentes tipos de usuários disponíveis  
- Ordenação e filtragem de produtos  
- Fluxo completo de compra (do carrinho até a finalização)  
- Remoção de itens do carrinho  
- Navegação entre páginas  
- Logout  

**Evidências:**  
As evidências (prints, anotações e relatórios) estão disponíveis no Terabox. Confira o link no documento [`docs/ui-testing/plano-testes.md`](docs/ui-testing/plano-testes.md).

---

## 2. API Testing (Restful-Booker)

**Objetivo:**  
Garantir que os principais endpoints da API [Restful-Booker](https://restful-booker.herokuapp.com) estejam funcionando corretamente, validando seu comportamento antes da integração com o front-end.

**Cenários Testados:**
- **Autenticação:**  
  - Gerar token de autenticação  
  - Tentar gerar token com credenciais inválidas  
- **Gestão de Reservas:**  
  - Criar, buscar, atualizar, listar e deletar reservas  
- **Filtros e Buscas:**  
  - Buscar reservas por nome  
  - Buscar reservas por data de check-in  
  - Buscar reservas por data de check-out  

**Evidências:**  
Os testes de API podem ser importados para o Postman usando o arquivo JSON neste repositório. A documentação detalhada encontra-se em [`docs/api-testing/plano-testes.md`](docs/api-testing/plano-testes.md).

### Como Importar para o Postman
1. Baixe o arquivo `api-testing-collection.json` localizado em `docs/api-testing/`.
2. No Postman, clique em **Import** (ícone de seta no canto superior esquerdo).
3. Selecione o arquivo baixado e importe a coleção.
4. Configure as variáveis de ambiente disponíveis na mesma pasta, se necessário.

---

## 📌 Como Reproduzir os Testes

### UI Testing
1. Acesse a aplicação em [https://www.saucedemo.com](https://www.saucedemo.com).
2. Consulte o documento [`docs/ui-testing/plano-testes.md`](docs/ui-testing/plano-testes.md) para o passo a passo de cada cenário (login, fluxo de compra, etc.).

### API Testing
1. Importe a collection do Postman disponível na pasta [`docs/api-testing/`](docs/api-testing/).
2. Configure as variáveis de ambiente incluídas na collection (se aplicável).
3. Consulte o documento [`docs/api-testing/plano-testes.md`](docs/api-testing/plano-testes.md) para detalhes sobre cada requisição e suas validações.

---

## 📌 Ferramentas Utilizadas 💻

### UI Testing
- **Navegadores:** Google Chrome e Microsoft Edge  
- **Lighthouse:** Verificação de acessibilidade e desempenho  
- **DevTools:** Inspeção e validação de tempos de resposta

### API Testing
- **Postman:** Criação, execução e organização das requisições de teste

---

## 📌 Colaborador ✨

**Edcleryton Gabriel** – Autor e responsável pelos testes

**Contato**  
- **E-mail:** [edcleryton.gabriel@gmail.com](mailto:edcleryton.gabriel@gmail.com)  
- **LinkedIn:** [Edcleryton Silva](https://www.linkedin.com/in/edcleryton-silva/)  
- **GitHub:** [Edcleryton](https://github.com/Edcleryton)

> **Nota:** Consulte os documentos indicados em `docs/ui-testing/` e `docs/api-testing/` para mais detalhes sobre planejamento, resultados, lista de bugs, análise de riscos e sugestões de melhorias.  

**Vamos garantir a qualidade!** 🚀
