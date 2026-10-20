## Cenário 24: Gestão de tipos de documentos.

### Caso de Teste 01: Adicionar novo tipo de documento.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C24-CT01 | O sistema deve permitir o cadastro de um tipo de documento. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Tipos de Documentos. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Tipos de Documentos"        |
| **E** clica em "Novo Tipo"                                        |
| **E** preenche "Nota fiscal" no Nome e escolhe a aplicação "Conta / Fornecedor" |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** o tipo de documento deve ser exibido na lista           |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O tipo de documento deve aparecer com a aplicação correta.      |

---

### Caso de Teste 02: Tentar adicionar tipo de documento sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C24-CT02 | O sistema deve impedir o cadastro sem nome.                |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Novo Tipo"                  |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O tipo de documento não deve ser salvo sem nome.                |

---

### Caso de Teste 03: Filtrar tipos de documentos por aplicação.

| ID       | Descrição                                                       |
| :------- | :-------------------------------------------------------------- |
| C24-CT03 | O sistema deve listar apenas os tipos da aplicação selecionada. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir tipos de documento cadastrados.                 |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Tipos de Documentos"        |
| **QUANDO** selecionar "Colaborador" no filtro Aplicação           |
| **ENTÃO** somente tipos aplicados a colaborador devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas a aplicação selecionada.            |
