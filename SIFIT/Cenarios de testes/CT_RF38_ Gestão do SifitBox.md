## Cenário 38: Gestão do SifitBox.

### Caso de Teste 01: Visualizar menu do SifitBox.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C38-CT01 | As telas de crossfit devem aparecer quando a academia for Box. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| A configuração "Academia marcada como Box?" deve estar como "Sim". |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está logado no sistema                     |
| **QUANDO** abrir o menu lateral                                   |
| **ENTÃO** os itens "SifitBox", "Box - Turmas" e "Categorias Crossfit" devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As telas de crossfit devem estar disponíveis no menu.           |

---

### Caso de Teste 02: Buscar aulas do SifitBox.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C38-CT02 | O sistema deve listar as aulas do período.                 |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O menu SifitBox deve estar disponível.                        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "SifitBox"                   |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** as aulas do período ou a mensagem "Nenhuma aula encontrada no periodo" devem ser exibidas |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A busca deve retornar as aulas corretamente.                    |

---

### Caso de Teste 03: Gerar aulas do SifitBox.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C38-CT03 | O sistema deve gerar as aulas a partir das turmas do Box.  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir ao menos uma turma do Box cadastrada.            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "SifitBox"                   |
| **QUANDO** clicar em "Gerar aulas"                                |
| **ENTÃO** as aulas devem ser criadas e exibidas na lista          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As aulas devem ser geradas e listadas.                          |
