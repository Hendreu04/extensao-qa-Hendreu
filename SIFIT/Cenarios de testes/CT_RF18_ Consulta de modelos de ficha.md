## Cenário 18: Consulta de modelos de ficha.

### Caso de Teste 01: Visualizar lista de modelos de ficha.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C18-CT01 | O sistema deve exibir os modelos de ficha cadastrados.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelo Ficha"               |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** a lista de modelos ou a mensagem "Nenhum modelo de ficha encontrado" deve ser exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A tela deve carregar corretamente.                              |

---

### Caso de Teste 02: Pesquisar modelo de ficha por título.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C18-CT02 | O sistema deve retornar o modelo pesquisado.               |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir ao menos um modelo de ficha cadastrado.          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelo Ficha"               |
| **E** digita o título de um modelo no campo Título                |
| **QUANDO** realizar a busca                                       |
| **ENTÃO** o modelo correspondente deve ser exibido                |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O modelo correspondente deve ser listado corretamente.          |

---

### Caso de Teste 03: Usar modelo ao cadastrar ficha de treino.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C18-CT03 | O modelo deve estar disponível no cadastro de ficha.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir ao menos um modelo de ficha cadastrado.          |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Ficha de Treino"            |
| **E** clica em "Cadastrar Ficha"                                  |
| **QUANDO** clicar em "Usar Modelo de Ficha"                       |
| **ENTÃO** os modelos cadastrados devem ser exibidos para seleção  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os modelos devem estar disponíveis para uso na ficha.           |
