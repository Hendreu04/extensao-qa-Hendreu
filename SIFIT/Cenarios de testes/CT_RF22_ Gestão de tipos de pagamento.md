## Cenário 22: Gestão de tipos de pagamento.

### Caso de Teste 01: Adicionar novo tipo de pagamento.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C22-CT01 | O sistema deve permitir o cadastro de um tipo de pagamento. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Tipos de Pagamento. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Tipos de Pagamento"         |
| **E** clica em "Novo"                                             |
| **E** preenche "Pix Hendreu" no Nome e escolhe o tipo "Débito"    |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** o tipo de pagamento deve ser exibido na lista           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O tipo de pagamento deve aparecer corretamente na lista.        |

---

### Caso de Teste 02: Tentar adicionar tipo de pagamento sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C22-CT02 | O sistema deve impedir o cadastro sem nome.                |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de cadastro de tipo de pagamento |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O tipo de pagamento não deve ser salvo sem nome.                |

---

### Caso de Teste 03: Filtrar tipos de pagamento por status.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C22-CT03 | O sistema deve listar apenas os tipos do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir tipos de pagamento cadastrados.                 |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Tipos de Pagamento"         |
| **QUANDO** selecionar "Inativo" no filtro Status                  |
| **ENTÃO** somente tipos inativos devem ser exibidos               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
