## Cenário 23: Gestão de bandeiras de cartão.

### Caso de Teste 01: Adicionar nova bandeira com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C23-CT01 | O sistema deve permitir o cadastro de uma bandeira.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Bandeiras.   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Bandeiras"                  |
| **E** clica em "Nova Bandeira"                                    |
| **E** preenche "Visa" no campo Nome                               |
| **QUANDO** salvar a bandeira                                      |
| **ENTÃO** a bandeira deve ser exibida na lista                    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A bandeira deve aparecer corretamente na lista.                 |

---

### Caso de Teste 02: Tentar adicionar bandeira sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C23-CT02 | O sistema deve impedir o cadastro de bandeira sem nome.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Bandeira"              |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar a bandeira                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A bandeira não deve ser salva sem nome.                         |

---

### Caso de Teste 03: Pesquisar bandeira já cadastrada.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C23-CT03 | O sistema deve retornar a bandeira pesquisada.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| A bandeira deve já estar cadastrada no sistema.               |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Bandeiras"                  |
| **E** digita "Visa" no campo Nome                                 |
| **QUANDO** realizar a busca                                       |
| **ENTÃO** a bandeira deve ser exibida na lista de resultados      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A bandeira correspondente deve ser listada corretamente.        |
