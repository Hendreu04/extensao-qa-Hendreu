## Cenário 15: Gestão de produtos.

### Caso de Teste 01: Adicionar novo produto com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C15-CT01 | O sistema deve permitir o cadastro de um produto.          |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Produtos.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Produtos"                   |
| **E** clica em "Novo"                                             |
| **E** preenche "Garrafa Hendreu" no Nome e escolhe o tipo "Venda" |
| **QUANDO** salvar o produto                                       |
| **ENTÃO** o produto deve ser exibido na lista com status "Ativo"  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O produto deve aparecer com o nome e o tipo corretos.           |

---

### Caso de Teste 02: Tentar adicionar produto sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C15-CT02 | O sistema deve impedir o cadastro de produto sem nome.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de cadastro de produto       |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o produto                                       |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O produto não deve ser salvo sem nome.                          |

---

### Caso de Teste 03: Filtrar produtos por tipo.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C15-CT03 | O sistema deve listar apenas os produtos do tipo selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir produtos de venda e de pontuação.               |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Produtos"                   |
| **QUANDO** selecionar "Pontuação" no filtro Tipo                  |
| **ENTÃO** somente produtos do tipo "Pontuação" devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o tipo selecionado.                 |
