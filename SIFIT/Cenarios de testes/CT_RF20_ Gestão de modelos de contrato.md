## Cenário 20: Gestão de modelos de contrato.

### Caso de Teste 01: Adicionar novo modelo de contrato.

| ID       | Descrição                                                    |
| :------- | :----------------------------------------------------------- |
| C20-CT01 | O sistema deve permitir o cadastro de um modelo de contrato. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Modelos Contrato. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelos Contrato"           |
| **E** clica em "Adicionar Modelo Contrato"                        |
| **E** preenche "Contrato Hendreu" no campo Nome e o texto do contrato |
| **QUANDO** salvar o modelo                                        |
| **ENTÃO** o modelo deve ser exibido na lista                      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O modelo deve aparecer corretamente na lista.                   |

---

### Caso de Teste 02: Tentar adicionar modelo de contrato sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C20-CT02 | O sistema deve impedir o cadastro de modelo sem nome.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de cadastro de modelo de contrato |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o modelo                                        |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O modelo não deve ser salvo sem nome.                           |

---

### Caso de Teste 03: Visualizar lista sem modelos cadastrados.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C20-CT03 | O sistema deve informar quando não houver modelos.         |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Não deve existir nenhum modelo de contrato cadastrado.        |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Modelos Contrato"           |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** uma mensagem informando que não há modelos deve ser exibida |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário deve ser avisado que a lista está vazia.              |
