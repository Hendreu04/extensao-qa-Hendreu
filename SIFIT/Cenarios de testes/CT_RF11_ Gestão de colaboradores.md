## Cenário 11: Gestão de colaboradores.

### Caso de Teste 01: Adicionar novo colaborador com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C11-CT01 | O sistema deve permitir o cadastro de um colaborador.      |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Colaboradores. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Colaboradores"              |
| **E** clica em "Novo Colaborador"                                 |
| **E** preenche "Hendreu Colaborador" no campo Nome e os demais campos obrigatórios |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** o colaborador deve ser exibido na lista com status "ATIVO" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O colaborador deve aparecer corretamente na lista.              |

---

### Caso de Teste 02: Tentar adicionar colaborador sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C11-CT02 | O sistema deve impedir o cadastro de colaborador sem nome. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela de cadastro de colaborador   |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar o cadastro                                      |
| **ENTÃO** uma mensagem de erro deve ser exibida no campo Nome     |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O colaborador não deve ser salvo sem nome.                      |

---

### Caso de Teste 03: Pesquisar colaborador já cadastrado.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C11-CT03 | O sistema deve retornar o colaborador pesquisado.          |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O colaborador deve já estar cadastrado no sistema.            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Colaboradores"              |
| **E** digita "Hendreu Colaborador" no campo Nome                  |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** o colaborador deve ser exibido na lista de resultados   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O colaborador correspondente deve ser listado corretamente.     |
