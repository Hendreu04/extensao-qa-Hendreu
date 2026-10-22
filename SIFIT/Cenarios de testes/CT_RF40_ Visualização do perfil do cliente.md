## Cenário 40: Visualização do perfil do cliente.

### Caso de Teste 01: Visualizar perfil do cliente.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C40-CT01 | O perfil deve exibir os dados do cliente corretamente.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente "Hendreu Teste" deve estar cadastrado.              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Clientes"                   |
| **QUANDO** clicar na lupa do cliente "Hendreu Teste"              |
| **ENTÃO** o perfil deve exibir o nome, a idade e a data de nascimento corretas |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os dados do perfil devem estar corretos.                        |

---

### Caso de Teste 02: Verificar matrícula atual no perfil.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C40-CT02 | O perfil deve mostrar a matrícula ativa do cliente.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve ter uma matrícula ativa.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está no perfil do cliente "Hendreu Teste"  |
| **QUANDO** verificar o bloco "Matrícula Atual"                    |
| **ENTÃO** o plano e as datas da matrícula devem ser exibidos      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A matrícula exibida deve ser a mesma da tela de Matrículas.     |

---

### Caso de Teste 03: Agendar avaliação pelo perfil.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C40-CT03 | A ação rápida deve abrir o agendamento de avaliação.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente deve estar cadastrado.                              |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está no perfil do cliente "Hendreu Teste"  |
| **QUANDO** clicar em "Agendar avaliação"                          |
| **ENTÃO** a tela de cadastro de avaliação deve ser aberta com o cliente já selecionado |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A ação rápida deve abrir a tela correta.                        |
