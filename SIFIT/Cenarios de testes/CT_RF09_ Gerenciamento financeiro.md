## Cenário 09: Gerenciamento financeiro.

### Caso de Teste 01: Cadastrar conta a receber com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C09-CT01 | O sistema deve permitir o cadastro de uma conta a receber. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve estar cadastrado no sistema.                   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Contas a Receber"           |
| **E** clica em "Nova Conta"                                       |
| **E** seleciona o cliente "Hendreu Teste", o valor "50,00" e a data de vencimento |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** a conta deve ser exibida na lista com status "PENDENTE" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A conta deve aparecer listada com o valor correto.              |

---

### Caso de Teste 02: Tentar cadastrar conta a receber sem valor.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C09-CT02 | O sistema deve impedir o cadastro de conta sem valor.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Conta a Receber"  |
| **E** deixa o campo "Valor a receber" em branco                   |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A conta não deve ser salva sem valor.                           |

---

### Caso de Teste 03: Verificar total das contas a pagar.

| ID       | Descrição                                                       |
| :------- | :-------------------------------------------------------------- |
| C09-CT03 | O total exibido deve corresponder às contas pendentes listadas. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir uma conta a pagar pendente.                      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Contas a Pagar"             |
| **E** filtra pelo status "Pendente"                               |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** o card "Total a Pagar" deve mostrar a soma das contas listadas |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O total deve ser igual à soma das contas pendentes.             |
