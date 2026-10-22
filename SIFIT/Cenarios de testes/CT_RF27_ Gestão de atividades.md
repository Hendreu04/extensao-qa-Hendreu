## Cenário 27: Gestão de atividades.

### Caso de Teste 01: Adicionar nova atividade com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C27-CT01 | O sistema deve permitir o cadastro de uma atividade.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Atividades.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Atividades"                 |
| **E** clica em "Nova Atividade"                                   |
| **E** preenche "Treinar 3x na semana" no Nome e "50" na pontuação |
| **QUANDO** salvar a atividade                                     |
| **ENTÃO** a atividade deve ser exibida na lista com 50 pts        |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A atividade deve aparecer com a pontuação correta.              |

---

### Caso de Teste 02: Tentar adicionar atividade sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C27-CT02 | O sistema deve impedir o cadastro de atividade sem nome.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Atividade"             |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar a atividade                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A atividade não deve ser salva sem nome.                        |

---

### Caso de Teste 03: Pesquisar atividade já cadastrada.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C27-CT03 | O sistema deve retornar a atividade pesquisada.            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| A atividade deve já estar cadastrada no sistema.              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Atividades"                 |
| **E** digita "Treinar 3x na semana" no campo Nome                 |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** a atividade deve ser exibida na lista de resultados     |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A atividade correspondente deve ser listada corretamente.       |
