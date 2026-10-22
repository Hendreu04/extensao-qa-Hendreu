## Cenário 28: Gestão de pontuações.

### Caso de Teste 01: Adicionar nova pontuação com dados válidos.

| ID       | Descrição                                                        |
| :------- | :--------------------------------------------------------------- |
| C28-CT01 | O sistema deve permitir o cadastro de uma campanha de pontuação. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Pontuação.   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Pontuação"                  |
| **E** clica em "Nova Pontuação"                                   |
| **E** preenche "Desafio de Novembro" no Nome e escolhe o tipo "Mensal" |
| **QUANDO** salvar a pontuação                                     |
| **ENTÃO** a pontuação deve ser exibida na lista com status "Ativo" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A pontuação deve aparecer corretamente na lista.                |

---

### Caso de Teste 02: Tentar adicionar pontuação sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C28-CT02 | O sistema deve impedir o cadastro de pontuação sem nome.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Pontuação"             |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar a pontuação                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A pontuação não deve ser salva sem nome.                        |

---

### Caso de Teste 03: Filtrar pontuações por status.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C28-CT03 | O sistema deve listar apenas as pontuações do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir pontuações cadastradas.                         |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Pontuação"                  |
| **E** seleciona "Ativo" no filtro Status                          |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente pontuações ativas devem ser exibidas            |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
