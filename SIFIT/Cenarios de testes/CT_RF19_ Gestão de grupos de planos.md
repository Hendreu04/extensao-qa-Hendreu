## Cenário 19: Gestão de grupos de planos.

### Caso de Teste 01: Visualizar lista de grupos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C19-CT01 | O sistema deve exibir os grupos cadastrados.               |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos cadastrados.                             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos"                     |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** a lista de grupos deve ser exibida com descrição, status e tipo de caixa |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os grupos devem ser exibidos corretamente.                      |

---

### Caso de Teste 02: Filtrar grupos por status.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C19-CT02 | O sistema deve listar apenas os grupos do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos cadastrados.                             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos"                     |
| **E** seleciona "Ativo" no filtro Status                          |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente grupos ativos devem ser exibidos                |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |

---

### Caso de Teste 03: Filtrar grupos por tipo de caixa.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C19-CT03 | O sistema deve listar apenas os grupos do tipo de caixa selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos cadastrados.                             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos"                     |
| **E** seleciona "Externo" no filtro Tipo Caixa                    |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente grupos com caixa externo devem ser exibidos, ou uma mensagem de nenhum resultado |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o tipo selecionado.                 |
