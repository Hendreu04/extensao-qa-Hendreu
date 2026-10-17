## Cenário 07: Cadastro de fichas de treino.

### Caso de Teste 01: Cadastrar ficha de treino com dados válidos.

| ID       | Descrição                                                        |
| :------- | :--------------------------------------------------------------- |
| C07-CT01 | O sistema deve permitir criar uma ficha de treino para um aluno. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente e um personal devem estar cadastrados.              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Ficha de Treino"            |
| **E** clica em "Cadastrar Ficha"                                  |
| **E** seleciona o aluno "Hendreu Teste", o personal e as datas    |
| **QUANDO** clicar em "Criar Nova Ficha"                           |
| **ENTÃO** a ficha deve ser exibida na lista de fichas             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A ficha deve aparecer listada com status ativo.                 |

---

### Caso de Teste 02: Tentar cadastrar ficha sem selecionar aluno.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C07-CT02 | O sistema deve impedir a criação de ficha sem aluno.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Ficha de Treino"  |
| **E** não seleciona nenhum aluno                                  |
| **QUANDO** clicar em "Criar Nova Ficha"                           |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A ficha não deve ser criada sem aluno.                          |

---

### Caso de Teste 03: Adicionar exercício em um grupo muscular.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C07-CT03 | O sistema deve permitir adicionar exercícios na biblioteca. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir um grupo muscular cadastrado.                    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Exercícios"                 |
| **E** clica em "Adicionar" no grupo "Pernas"                      |
| **E** preenche o nome "Agachamento"                               |
| **QUANDO** salvar o exercício                                     |
| **ENTÃO** o exercício deve aparecer no grupo "Pernas"             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O exercício deve ser listado no grupo correto.                  |
