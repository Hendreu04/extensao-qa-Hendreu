## Cenário 12: Gestão de funções.

### Caso de Teste 01: Adicionar nova função com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C12-CT01 | O sistema deve permitir o cadastro de uma função.          |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Funções.     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Funções"                    |
| **E** clica em "Nova Função"                                      |
| **E** preenche "Recepcionista Hendreu" no Nome e escolhe o tipo "Interno" |
| **QUANDO** salvar a função                                        |
| **ENTÃO** a função deve ser exibida na lista de funções           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A função deve aparecer com o nome e o tipo corretos.            |

---

### Caso de Teste 02: Tentar adicionar função sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C12-CT02 | O sistema deve impedir o cadastro de função sem nome.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Função"                |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar a função                                        |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A função não deve ser salva sem nome.                           |

---

### Caso de Teste 03: Filtrar funções por tipo.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C12-CT03 | O sistema deve listar apenas as funções do tipo selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir funções internas e externas.                    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Funções"                    |
| **E** seleciona "Externo" no filtro Tipo                          |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente funções do tipo "Externo" devem ser exibidas    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o tipo selecionado.                 |
