## Cenário 03: Gestão de clientes.

### Caso de Teste 01: Adicionar novo cliente com dados válidos.

| ID       | Descrição                                                           |
| :------- | :------------------------------------------------------------------ |
| C03-CT01 | O sistema deve permitir o cadastro de um cliente com dados válidos. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Clientes.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Clientes"                   |
| **E** clica em "Novo Cliente"                                     |
| **E** preenche "Hendreu Teste" no campo Nome, o sexo e a data de nascimento |
| **QUANDO** clicar em "Cadastrar Cliente"                          |
| **ENTÃO** o cliente deve ser cadastrado e exibido na lista de clientes |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente deve aparecer corretamente na lista de clientes.      |

---

### Caso de Teste 02: Tentar adicionar cliente sem preencher campos obrigatórios.

| ID       | Descrição                                                                           |
| :------- | :---------------------------------------------------------------------------------- |
| C03-CT02 | O sistema deve exibir erros ao tentar salvar um cliente sem os campos obrigatórios. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Cadastrar Cliente"          |
| **E** deixa os campos obrigatórios em branco                      |
| **QUANDO** clicar em "Cadastrar Cliente"                          |
| **ENTÃO** mensagens de erro devem ser exibidas nos campos obrigatórios |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os campos obrigatórios devem exibir mensagens de validação.     |

---

### Caso de Teste 03: Pesquisar cliente já cadastrado.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C03-CT03 | O sistema deve retornar corretamente o cliente pesquisado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve já estar cadastrado no sistema.                |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Clientes"                   |
| **E** digita "Hendreu Teste" no campo Nome                        |
| **QUANDO** clicar no botão "Buscar"                               |
| **ENTÃO** o sistema deve exibir "Hendreu Teste" na lista de resultados |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O cliente correspondente deve ser listado corretamente.         |
