## Cenário 31: Gestão de modelos de anamnese.

### Caso de Teste 01: Adicionar novo modelo de anamnese.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C31-CT01 | O sistema deve permitir o cadastro de um modelo de anamnese. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir ao menos uma pergunta de anamnese cadastrada.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelos"                    |
| **E** clica em "Novo Modelo"                                      |
| **E** preenche "Modelo Hendreu" no Nome e adiciona uma pergunta   |
| **QUANDO** salvar o modelo                                        |
| **ENTÃO** o modelo deve ser exibido na lista com 1 pergunta       |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O modelo deve aparecer com a quantidade de perguntas correta.   |

---

### Caso de Teste 02: Visualizar prévia do modelo.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C31-CT02 | O sistema deve mostrar a prévia do questionário.           |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir um modelo de anamnese cadastrado.                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelos"                    |
| **QUANDO** clicar em "Preview" em um modelo                       |
| **ENTÃO** as perguntas do modelo devem ser exibidas como o aluno verá |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A prévia deve exibir as perguntas do modelo.                    |

---

### Caso de Teste 03: Filtrar modelos por status.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C31-CT03 | O sistema deve listar apenas os modelos do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir modelos cadastrados.                            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelos"                    |
| **QUANDO** selecionar "Inativo" no filtro de status               |
| **ENTÃO** somente modelos inativos devem ser exibidos             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
