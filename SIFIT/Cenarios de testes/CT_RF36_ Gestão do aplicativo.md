## Cenário 36: Gestão do aplicativo.

### Caso de Teste 01: Criar notificação para os alunos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C36-CT01 | O sistema deve permitir criar uma notificação.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Aplicativo.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Aplicativo"                 |
| **E** clica em "Criar Notificação"                                |
| **E** preenche a mensagem "Teste de aviso - Hendreu"              |
| **QUANDO** salvar a notificação                                   |
| **ENTÃO** a notificação deve ser exibida na lista com a data de hoje |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A notificação deve aparecer corretamente na lista.              |

---

### Caso de Teste 02: Tentar criar notificação sem mensagem.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C36-CT02 | O sistema deve impedir notificação sem texto.              |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Criar Notificação"          |
| **E** deixa a mensagem em branco                                  |
| **QUANDO** salvar a notificação                                   |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A notificação não deve ser salva sem mensagem.                  |

---

### Caso de Teste 03: Filtrar postagens pendentes.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C36-CT03 | O sistema deve listar apenas as postagens pendentes de aprovação. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Aplicativo"                 |
| **QUANDO** marcar a opção "Só pendentes" em Postagens             |
| **ENTÃO** somente postagens pendentes devem ser exibidas          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas as postagens pendentes.             |
