## Cenário 10: Geração e visualização de relatórios.

### Caso de Teste 01: Gerar relatório de clientes.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C10-CT01 | O sistema deve gerar o relatório de clientes em PDF.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir clientes cadastrados.                           |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Relatórios"                 |
| **E** seleciona o tipo "Clientes"                                 |
| **E** informa a data de início e de fim                           |
| **QUANDO** clicar em "Gerar Relatório"                            |
| **ENTÃO** o relatório deve ser exibido em PDF                     |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O relatório deve ser gerado com os dados do período.            |

---

### Caso de Teste 02: Gerar relatório com data de início maior que a de fim.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C10-CT02 | O sistema deve impedir a geração com período inválido.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Relatórios"                 |
| **E** informa a data de início maior que a data de fim            |
| **QUANDO** clicar em "Gerar Relatório"                            |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O relatório não deve ser gerado com período inválido.           |

---

### Caso de Teste 03: Gerar relatório sem registros no período.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C10-CT03 | O sistema deve informar quando não houver dados no período. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Relatórios"                 |
| **E** informa um período sem nenhum registro                      |
| **QUANDO** clicar em "Gerar Relatório"                            |
| **ENTÃO** o sistema deve informar que não há registros            |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário deve ser avisado que não existem dados no período.    |
