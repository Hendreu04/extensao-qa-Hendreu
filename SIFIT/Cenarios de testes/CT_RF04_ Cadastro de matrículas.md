## Cenário 04: Cadastro de matrículas.

### Caso de Teste 01: Cadastrar matrícula com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT01 | O sistema deve permitir matricular um cliente em um plano. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve estar cadastrado e existir um plano ativo.     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Matrículas"                 |
| **E** clica em "Cadastrar Matrícula"                              |
| **E** seleciona o cliente "Hendreu Teste" e o plano "Plano Diário" |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** a matrícula deve ser exibida na lista com status "ATIVO" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A matrícula deve aparecer listada com o plano correto.          |

---

### Caso de Teste 02: Tentar cadastrar matrícula sem selecionar cliente.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C04-CT02 | O sistema deve impedir a matrícula sem cliente selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Matrícula"        |
| **E** não seleciona nenhum cliente                                |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A matrícula não deve ser salva e o erro deve ser exibido ao usuário. |

---

### Caso de Teste 03: Cadastrar matrícula com data final anterior à inicial.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C04-CT03 | O sistema deve impedir um período de matrícula inválido.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve estar cadastrado no sistema.                   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Matrícula"        |
| **E** seleciona o cliente e o plano                               |
| **E** informa a data final anterior à data inicial                |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida sobre as datas    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema não deve aceitar o período inválido.                  |
