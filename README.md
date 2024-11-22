# Teste Prático QA Testing BeTalent

Este repositório contém a documentação e as evidências dos testes realizados para o desafio QA Testing BeTalent. Os testes estão divididos em dois tipos principais: **UI Testing** e **API Testing**.

---

## Estrutura do Repositório

- **`README.md`**: Este arquivo, contendo as instruções e informações gerais.
- **`docs/`**:
  - `plano-testes.md`: Documento com os planos de testes detalhados.
- **`Evidencias/`**: Contém as capturas de tela e arquivos de evidências organizados:
  - **`ui-testing/`**:
    - `login/`: Evidências de login.
    - `ordenacao/`: Evidências de ordenação e filtros.
    - `fluxo_compra/`: Evidências do fluxo completo de compra.
    - `logout/`: Evidências de logout.
  - **`api-testing/`**:
    - `autenticacao/`: Evidências de autenticação.
    - `reservas/`: Evidências de gestão de reservas.

---

## Testes Realizados

### 1. UI Testing (Sauce Demo)

#### **Objetivo**
Validar os principais fluxos de funcionalidade e usabilidade da plataforma Sauce Demo para garantir que esteja pronta para lançamento em produção.

#### **Cenários Testados**
1. **Login com diferentes tipos de usuários disponíveis**
2. **Ordenação e filtragem de produtos**
3. **Fluxo completo de compra (do carrinho até finalização)**
4. **Remoção de itens do carrinho**
5. **Navegação entre páginas**
6. **Logout**

#### **Evidências**
As evidências dos testes manuais estão organizadas na pasta `Evidencias/ui-testing/`, separadas por cenário.

#### **Como Reproduzir**
1. Acesse a aplicação Sauce Demo: [https://www.saucedemo.com](https://www.saucedemo.com).
2. Consulte o documento `docs/plano-testes.md` para os passos detalhados de cada cenário de teste.
3. Verifique as evidências capturadas na pasta correspondente.

---

### 2. API Testing (Restful-Booker)

#### **Objetivo**
Garantir que os principais endpoints da API Restful-Booker estejam funcionando corretamente antes da integração com o front-end.

#### **Cenários Testados**
1. **Autenticação**
   - Gerar token de autenticação.
   - Testar autenticação com credenciais inválidas.
2. **Gestão de Reservas**
   - Criar, buscar, atualizar, listar e deletar reservas.
3. **Filtros e Buscas**
   - Buscar reservas por nome, data de check-in e data de check-out.

#### **Evidências**
As evidências dos testes de API estão organizadas na pasta `Evidencias/api-testing/`, separadas por cenário.

#### **Como Reproduzir**
1. Importe a collection do Postman disponível na pasta `collections/` (se aplicável).
2. Configure as variáveis de ambiente incluídas na collection.
3. Consulte o documento `docs/plano-testes.md` para os passos detalhados de cada cenário.
4. Verifique as evidências capturadas na pasta correspondente.

---

## Observações Gerais

- **Ferramentas Utilizadas**:
  - **UI Testing**: Testes manuais utilizando navegadores (Google Chrome, Firefox).
  - **API Testing**: Postman para criação e execução de testes em endpoints da API.
- **Organização**:
  - Todas as evidências estão organizadas em pastas para facilitar a análise.
  - O plano de testes está documentado em formato Markdown no arquivo `docs/plano-testes.md`.

---

## Contribuição

Este repositório foi estruturado para garantir clareza e organização. Caso tenha dúvidas ou sugestões, sinta-se à vontade para abrir uma **issue** ou entrar em contato.

---

**Boa sorte e sucesso nos testes!**
