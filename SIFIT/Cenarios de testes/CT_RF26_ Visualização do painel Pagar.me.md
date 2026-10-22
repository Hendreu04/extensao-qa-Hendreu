## Cenário 26: Visualização do painel Pagar.me.

### Caso de Teste 01: Visualizar painel da Pagar.me.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C26-CT01 | O sistema deve exibir o painel de recebimentos.            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Pagar.me"                   |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** devem ser exibidos os saldos, o gráfico de recebimentos e os meios de pagamento |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O painel deve carregar corretamente.                            |

---

### Caso de Teste 02: Verificar coerência dos valores de recebimento.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C26-CT02 | Os valores do gráfico devem corresponder aos saldos e transações. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Pagar.me"                   |
| **QUANDO** comparar o total de recebimentos com os valores por meio de pagamento e as transações recentes |
| **ENTÃO** os valores devem ser coerentes entre si                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As informações do painel não devem se contradizer.              |

---

### Caso de Teste 03: Visualizar transações recentes.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C26-CT03 | O sistema deve listar as transações recentes.              |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Pagar.me"                   |
| **QUANDO** clicar em "Ver todas as transações"                    |
| **ENTÃO** a lista de transações deve ser exibida, ou uma mensagem de que não há transações |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As transações devem ser exibidas corretamente.                  |
