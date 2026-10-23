## Cenário 05: Gerenciamento de planos.

### Caso de Teste 01: Adicionar novo plano com dados válidos.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C05-CT01 | O sistema deve permitir o cadastro de um plano com dados válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Planos.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Planos"                     |
| **E** clica em "Novo Plano"                                       |
| **E** preenche "Plano Hendreu" no Nome e "99,90" no Valor Mensal  |
| **QUANDO** clicar em "Salvar Plano"                               |
| **ENTÃO** o plano deve ser exibido na lista de planos             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O plano deve aparecer com o nome e o valor corretos.            |

---

### Caso de Teste 02: Tentar adicionar plano sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C05-CT02 | O sistema deve impedir o cadastro de plano sem nome.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Novo Plano"                 |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** clicar em "Salvar Plano"                               |
| **ENTÃO** uma mensagem de erro deve ser exibida no campo Nome     |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O plano não deve ser salvo sem nome.                            |

---

### Caso de Teste 03: Verificar quantidade de alunos por plano.

| ID       | Descrição                                                                |
| :------- | :----------------------------------------------------------------------- |
| C05-CT03 | A quantidade de alunos deve ser a mesma no ranking e na lista de planos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir um plano com alunos matriculados.                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Planos"                     |
| **QUANDO** verificar a quantidade de alunos do plano "Teste Diaria QA Verify" no ranking e na lista |
| **ENTÃO** a quantidade deve ser a mesma nos dois lugares          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As informações do plano devem ser iguais em toda a tela.        |
