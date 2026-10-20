## Cenário 14: Gestão de leads na prospecção.

### Caso de Teste 01: Adicionar novo lead com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C14-CT01 | O sistema deve permitir o cadastro de um lead.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Prospecção.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Prospecção"                 |
| **E** clica em "Adicionar Lead"                                   |
| **E** preenche "Lead Hendreu" no campo Nome                       |
| **QUANDO** salvar o lead                                          |
| **ENTÃO** o lead deve ser exibido na lista com o estágio "Novo Contato" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O lead deve aparecer na lista com o estágio correto.            |

---

### Caso de Teste 02: Tentar adicionar lead sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C14-CT02 | O sistema deve impedir o cadastro de lead sem nome.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Adicionar Lead"             |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o lead                                          |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O lead não deve ser salvo sem nome.                             |

---

### Caso de Teste 03: Filtrar leads por estágio.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C14-CT03 | O sistema deve listar apenas os leads do estágio selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir leads em estágios diferentes.                   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Prospecção"                 |
| **QUANDO** selecionar "Interessado" no filtro Estágio             |
| **ENTÃO** somente leads com o estágio "Interessado" devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o estágio selecionado.              |
