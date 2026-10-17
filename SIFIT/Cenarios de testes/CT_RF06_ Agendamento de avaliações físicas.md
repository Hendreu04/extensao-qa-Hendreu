## Cenário 06: Agendamento de avaliações físicas.

### Caso de Teste 01: Agendar avaliação com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C06-CT01 | O sistema deve permitir agendar uma avaliação física.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente e um personal devem estar cadastrados.              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Avaliações"                 |
| **E** clica em "Cadastrar Avaliação"                              |
| **E** seleciona o aluno "Hendreu Teste", o personal, a data e a hora |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** a avaliação deve ser exibida na lista com status "pendente" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A avaliação deve aparecer listada corretamente.                 |

---

### Caso de Teste 02: Tentar agendar avaliação sem selecionar aluno.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C06-CT02 | O sistema deve impedir o agendamento sem aluno.            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Avaliação"        |
| **E** não seleciona nenhum aluno                                  |
| **QUANDO** clicar em "Salvar"                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A avaliação não deve ser salva sem aluno.                       |

---

### Caso de Teste 03: Filtrar avaliações por status.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C06-CT03 | O sistema deve listar apenas as avaliações do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir avaliações pendentes e realizadas.              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Avaliações"                 |
| **E** seleciona "Pendente" no filtro Status                       |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente avaliações pendentes devem ser exibidas         |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
