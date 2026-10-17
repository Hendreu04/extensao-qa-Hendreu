## Cenário 08: Turmas e check-in.

### Caso de Teste 01: Cadastrar turma com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C08-CT01 | O sistema deve permitir o cadastro de uma turma.           |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Turmas.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Turmas"                     |
| **E** clica em "Cadastrar Turma"                                  |
| **E** preenche o nome "Turma Hendreu", o horário de 07:00 às 08:00 e os dias |
| **QUANDO** salvar a turma                                         |
| **ENTÃO** a turma deve ser exibida na lista de turmas             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A turma deve aparecer com o horário e os dias corretos.         |

---

### Caso de Teste 02: Tentar cadastrar turma com horário final igual ao inicial.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C08-CT02 | O sistema deve impedir turma com horário inválido.         |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Turma"            |
| **E** preenche o horário de 08:00 às 08:00                        |
| **QUANDO** salvar a turma                                         |
| **ENTÃO** uma mensagem de erro deve ser exibida sobre o horário   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A turma não deve ser salva com horário inválido.                |

---

### Caso de Teste 03: Realizar check-in manual do aluno.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C08-CT03 | O sistema deve registrar o check-in pelo código do cliente. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve ter matrícula ativa.                           |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Check-in"                   |
| **E** digita o código do cliente em "Entrada rápida"              |
| **QUANDO** clicar em "Realizar check-in"                          |
| **ENTÃO** o cliente deve aparecer na lista de presentes           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O check-in deve ser registrado e exibido na tela.               |
