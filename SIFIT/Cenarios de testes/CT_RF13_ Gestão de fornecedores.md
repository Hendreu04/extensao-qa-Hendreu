## Cenário 13: Gestão de fornecedores.

### Caso de Teste 01: Adicionar novo fornecedor com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C13-CT01 | O sistema deve permitir o cadastro de um fornecedor.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Fornecedores. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Fornecedores"               |
| **E** clica em "Novo Fornecedor"                                  |
| **E** preenche "Fornecedor Hendreu" no campo Nome                 |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** o fornecedor deve ser exibido na lista com status "ATIVO" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O fornecedor deve aparecer corretamente na lista.               |

---

### Caso de Teste 02: Tentar adicionar fornecedor sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C13-CT02 | O sistema deve impedir o cadastro de fornecedor sem nome.  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de cadastro de fornecedor    |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O fornecedor não deve ser salvo sem nome.                       |

---

### Caso de Teste 03: Pesquisar fornecedor já cadastrado.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C13-CT03 | O sistema deve retornar o fornecedor pesquisado.           |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O fornecedor deve já estar cadastrado no sistema.             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Fornecedores"               |
| **E** digita "Fornecedor Hendreu" no campo Nome                   |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** o fornecedor deve ser exibido na lista de resultados    |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O fornecedor correspondente deve ser listado corretamente.      |
