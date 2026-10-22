## Cenário 34: Visualização das automações.

### Caso de Teste 01: Visualizar automações ativas.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C34-CT01 | O sistema deve exibir as automações ativas.                |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Inteligência & Automação"   |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** as automações ativas devem ser exibidas com frequência, canal e última execução |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As automações devem ser exibidas corretamente.                  |

---

### Caso de Teste 02: Abrir os resultados de uma automação.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C34-CT02 | O botão de resultados deve abrir a tela correspondente.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Deve existir uma automação já executada.                      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Inteligência & Automação"   |
| **QUANDO** clicar em "Ver resultados" na automação "Risco de Evasão" |
| **ENTÃO** a tela de resultados da inteligência deve ser exibida   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O usuário deve ser levado aos resultados da automação.          |

---

### Caso de Teste 03: Atualizar a central de automações.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C34-CT03 | O botão Atualizar deve recarregar as informações.          |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Inteligência & Automação"   |
| **QUANDO** clicar em "Atualizar"                                  |
| **ENTÃO** as informações das automações devem ser recarregadas sem erro |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A tela deve ser atualizada corretamente.                        |
