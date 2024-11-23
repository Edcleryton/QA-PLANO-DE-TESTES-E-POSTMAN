# Registro de Bugs - Sauce Demo e Restful-Booker

## Índice
1. [Detalhes dos Bugs](#detalhes-dos-bugs)  
2. [Resumo Geral](#resumo-geral)  

---

## Detalhes dos Bugs

| **ID**      | **Título**                                         | **Passo-a-passo**                                                                                                                                                           | **Objetivo**                                                                                | **Versão** | **Plataforma** | **Navegador**     | **Criticidade** | **Status** | **Evidência**                                                                                              | **Caso de Teste Relacionado** |
|-------------|---------------------------------------------------|---------------------------------------------------------------------------------------------------------------------------------------------------------------------------|--------------------------------------------------------------------------------------------|------------|----------------|-------------------|-----------------|------------|------------------------------------------------------------------------------------------------------------|--------------------------------|
| BUG-0001    | Tempo de resposta no login acima do esperado       | **Dado:** que o usuário está na página de login.<br>**Quando:** insere credenciais válidas e clica em "Login".<br>**Então:** o tempo de resposta é superior ao esperado (3.54s). | Garantir que o tempo de resposta no login seja inferior a 2 segundos.                      | 1          | Windows        | Chrome/Edge       | Alta            | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | LG-NF-002                      |
| BUG-0002    | Mensagem de erro genérica ao falhar login          | **Dado:** que o usuário está na página de login.<br>**Quando:** insere credenciais inválidas e clica em "Login".<br>**Então:** é exibida uma mensagem de erro genérica.      | Informar de forma clara que as credenciais estão incorretas.                                | 1          | Windows        | Chrome/Edge       | Moderada        | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | LG-002                        |
| BUG-0003    | Login não funcional em dispositivos móveis         | **Dado:** que o usuário acessa o site pelo dispositivo móvel POCO X6 PRO (Android 14).<br>**Quando:** tenta acessar a página de login.<br>**Então:** a página não carrega.  | Permitir login funcional em dispositivos móveis compatíveis com os navegadores Chrome/Edge. | 1          | Android 14     | Chrome/Edge       | Alta            | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | LG-NF-004                      |
| BUG-0004    | Login com falha de layout                         | **Dado:** que o usuário está na página de login.<br>**Quando:** insere credenciais do usuário `problem_user` e clica em "Login".<br>**Então:** os elementos estão desalinhados. | Garantir que os elementos da interface estejam corretamente alinhados.                     | 1          | Windows        | Chrome/Edge       | Moderada        | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | LG-008                        |
| BUG-0005    | Checkout incompleto - Falta de validação obrigatória | **Dado:** que o usuário acessa o checkout.<br>**Quando:** preenche apenas "Nome", "Sobrenome" e "Código Postal" e tenta finalizar a compra.<br>**Então:** o sistema não solicita informações de pagamento e permite a conclusão do pedido. | Garantir que todos os campos obrigatórios sejam validados antes de finalizar a compra.     | 1          | Windows        | Chrome/Edge       | Crítica         | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | FC-004                        |
| BUG-0006    | Ausência de opções de pagamento no checkout        | **Dado:** que o usuário acessa a página de checkout.<br>**Quando:** revisa os itens e tenta concluir a compra.<br>**Então:** não há opções ou campos disponíveis para selecionar o método de pagamento. | Implementar opções de pagamento (cartão, boleto, etc.) como parte obrigatória do checkout. | 1          | Windows        | Chrome/Edge       | Crítica         | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | FC-003                        |
| BUG-0007    | Falha de acessibilidade no checkout                | **Dado:** que o usuário tenta usar o checkout apenas com o teclado.<br>**Quando:** navega usando Tab e Enter.<br>**Então:** não há foco visível nos botões e campos, e ações inesperadas são realizadas. | Garantir que todos os elementos sejam acessíveis via teclado, com foco visível.           | 1          | Windows        | Chrome/Edge       | Moderada        | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | FC-NF-004                      |
| BUG-0008    | Finalização de compra com carrinho vazio           | **Dado:** que o usuário acessa o checkout sem itens no carrinho.<br>**Quando:** preenche os dados no checkout e tenta finalizar a compra.<br>**Então:** a finalização é feita com sucesso, mesmo sem produtos. | Bloquear o processo de checkout quando o carrinho estiver vazio.                          | 1          | Windows        | Chrome/Edge       | Crítica         | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | RC-002                        |
| BUG-0009    | Página "About" redireciona para conteúdo externo desconhecido | **Dado:** que o usuário acessa o menu "About".<br>**Quando:** clica na opção.<br>**Então:** é redirecionado para a página da Sauce Labs sem contexto claro ou documentação. | Documentar o redirecionamento da opção "About" ou corrigir o comportamento.                | 1          | Windows        | Chrome/Edge       | Moderada        | Aberto     | [Ver Evidência](https://terabox.com/s/1n6mXASr--7qBy0lObrCBZg)                                            | NP-005                        |

---

## Resumo Geral

- **Total de Bugs Registrados:** 9
- **Bugs Críticos/Bloqueadores:** 3
- **Bugs Moderados:** 5
- **Bugs Leves:** 0
- **Status Atual dos Bugs:**
  - **Abertos:** 9
  - **Fechados:** 0

### Notas Adicionais
- **Priorização:** Os bugs de maior criticidade devem ser tratados antes do lançamento.
- **Acompanhamento:** As evidências e casos relacionados estão documentados para facilitar a resolução.
- **Próximos Passos:** Executar retestes após a correção dos bugs.

> **Nota:** Consulte o [Plano de Testes](./plano-testes.md) e o [Relatório de Resultados](./relatorio-resultados.md) para mais detalhes.
