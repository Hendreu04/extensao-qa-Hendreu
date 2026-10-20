## Cenário 17: Gestão de objetivos de treino.

### Caso de Teste 01: Adicionar novo objetivo com dados válidos.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C17-CT01 | O sistema deve permitir o cadastro de um objetivo de treino. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Objetivos Treino. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Objetivos Treino"           |
| **E** clica em "Novo Objetivo"                                    |
| **E** preenche "Hipertrofia" no campo Nome                        |
| **QUANDO** salvar o objetivo                                      |
| **ENTÃO** o objetivo deve ser exibido na lista                    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O objetivo deve aparecer corretamente na lista.                 |

---

### Caso de Teste 02: Tentar adicionar objetivo sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C17-CT02 | O sistema deve impedir o cadastro de objetivo sem nome.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Novo Objetivo"              |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o objetivo                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O objetivo não deve ser salvo sem nome.                         |

---

### Caso de Teste 03: Pesquisar objetivo já cadastrado.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C17-CT03 | O sistema deve retornar o objetivo pesquisado.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O objetivo deve já estar cadastrado no sistema.               |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Objetivos Treino"           |
| **E** digita "Hipertrofia" no campo Nome                          |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** o objetivo deve ser exibido na lista de resultados      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O objetivo correspondente deve ser listado corretamente.        |
