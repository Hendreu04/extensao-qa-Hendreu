## Cenário 39: Acesso e visualização do Dashboard.

### Caso de Teste 01: Acesso ao Dashboard pelo menu.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C39-CT01 | Verificar a exibição correta do Dashboard.                 |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está logado no sistema                     |
| **QUANDO** clicar no menu "Dashboard"                             |
| **ENTÃO** a tela deve ser exibida com o título "Dashboard" e os gráficos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O Dashboard deve ser exibido com o título correto.              |

---

### Caso de Teste 02: Verificação dos gráficos do Dashboard.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C39-CT02 | Os gráficos devem ser exibidos com os dados da academia.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está no Dashboard                          |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** os gráficos de Clientes, Matrículas, Contas a Receber, Cancelamentos e Avaliações devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todos os gráficos devem ser visíveis.                           |

---

### Caso de Teste 03: Abrir a Inteligência pelo Dashboard.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C39-CT03 | O botão deve levar à tela de inteligência.                 |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está no Dashboard                          |
| **QUANDO** clicar em "Ver Inteligência"                           |
| **ENTÃO** a tela de inteligência deve ser exibida                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário deve ser levado à tela correta.                       |
