# Teste Prático QA Testing BeTalent

Este repositório contém os resultados e evidências de dois tipos de testes realizados como parte do Teste Prático QA Testing BeTalent:

1. **UI Testing (Sauce Demo)**
2. **API Testing (Restful-Booker)**

## Estrutura do Repositório

- **`plano-testes.md`**: Documento que detalha o plano de testes para ambos os contextos.
- **`evidencias/`**: Pasta com as evidências organizadas por tipo de teste e cenário.
  - **`ui-testing/`**: Evidências do teste da interface do usuário.
  - **`api-testing/`**: Evidências do teste de API.
- **`collections/`**: Arquivo com a collection do Postman configurada para o teste de API (inclui variáveis de ambiente e exemplos de requisições).

## Testes Realizados

### 1. UI Testing (Sauce Demo)

#### Objetivo
Testar os principais fluxos da aplicação de e-commerce **Sauce Demo**, garantindo que a interface do usuário funcione corretamente antes do lançamento.

#### Cenários Testados
- **Login com diferentes tipos de usuários disponíveis**
- **Ordenação e filtragem de produtos**
- **Fluxo completo de compra (do carrinho até finalização)**
- **Remoção de itens do carrinho**
- **Navegação entre páginas**
- **Logout**

#### Como Reproduzir os Testes
1. Acesse o site [Sauce Demo](https://www.saucedemo.com).
2. Consulte o documento `plano-testes.md` para os detalhes de cada caso de teste.
3. Verifique as evidências na pasta `evidencias/ui-testing`.

---

### 2. API Testing (Restful-Booker)

#### Objetivo
Validar os principais endpoints da API **Restful-Booker**, garantindo que estejam funcionais antes da integração com o front-end.

#### Cenários Testados
- **Autenticação**
  - Gerar token de autenticação
  - Testar autenticação com credenciais inválidas
- **Gestão de Reservas**
  - Criar, buscar, atualizar, listar e deletar reservas
- **Filtros e Buscas**
  - Buscar reservas por nome, data de check-in e data de check-out

#### Como Reproduzir os Testes
1. Importe a collection disponível na pasta `collections/` para o Postman.
2. Configure as variáveis de ambiente (incluídas no arquivo).
3. Consulte o documento `plano-testes.md` para os detalhes de cada caso de teste.
4. Verifique as evidências na pasta `evidencias/api-testing`.

---

## Observações Gerais

- **Ferramentas Utilizadas**:
  - **UI Testing**: Testes manuais utilizando navegadores (Google Chrome, Firefox) e capturas de tela para evidências.
  - **API Testing**: Postman para criação e execução de testes em endpoints da API.
- **Organização do Código**:
  - Todos os arquivos estão organizados por tipo de teste e cenário, facilitando a navegação e análise.

## Como Subir as Evidências no GitHub

1. Certifique-se de que todas as capturas de tela e arquivos estejam organizados nas respectivas pastas.
2. Faça o commit das evidências:
   ```bash
   git add evidencias/
   git commit -m "Adicionando evidências dos testes UI e API"
   git push
