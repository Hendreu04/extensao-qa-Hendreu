## Cenário 33: Gestão de perguntas de anamnese.

### Caso de Teste 01: Adicionar nova pergunta com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C33-CT01 | O sistema deve permitir o cadastro de uma pergunta.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir uma categoria de anamnese ativa.                 |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Perguntas"                  |
| **E** clica em "Nova Pergunta"                                    |
| **E** preenche "Possui alguma lesão?" e escolhe a categoria       |
| **QUANDO** salvar a pergunta                                      |
| **ENTÃO** a pergunta deve ser exibida na lista com status "ATIVO" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A pergunta deve aparecer corretamente na lista.                 |

---

### Caso de Teste 02: Tentar adicionar pergunta em branco.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C33-CT02 | O sistema deve impedir o cadastro de pergunta sem texto.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Pergunta"              |
| **E** deixa o texto da pergunta em branco                         |
| **QUANDO** salvar a pergunta                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A pergunta não deve ser salva sem texto.                        |

---

### Caso de Teste 03: Pesquisar pergunta já cadastrada.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C33-CT03 | O sistema deve retornar a pergunta pesquisada.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| A pergunta deve já estar cadastrada no sistema.               |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Perguntas"                  |
| **E** digita "lesão" no campo Nome                                |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** a pergunta deve ser exibida na lista de resultados      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A pergunta correspondente deve ser listada corretamente.        |
