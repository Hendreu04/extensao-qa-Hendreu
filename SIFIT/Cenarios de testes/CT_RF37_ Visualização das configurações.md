## Cenário 37: Visualização das configurações.

### Caso de Teste 01: Visualizar configurações gerais.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C37-CT01 | O sistema deve exibir as configurações da academia.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Configurações"              |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** a aba "Home" deve ser exibida com as configurações de acesso e presença |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| As configurações devem ser exibidas corretamente.               |

---

### Caso de Teste 02: Navegar entre as abas de configuração.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C37-CT02 | As abas devem exibir as configurações correspondentes.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Configurações"              |
| **QUANDO** clicar nas abas "Biometria", "Avaliação" e "Pagamento" |
| **ENTÃO** cada aba deve exibir suas configurações                 |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todas as abas devem abrir corretamente.                         |

---

### Caso de Teste 03: Cancelar alteração de configuração.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C37-CT03 | Ao cancelar, nenhuma alteração deve ser salva.             |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Configurações"              |
| **E** altera o campo "Dias para contar cliente como ausente"      |
| **QUANDO** clicar em "Cancelar"                                   |
| **ENTÃO** a configuração deve continuar com o valor anterior      |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Nenhuma configuração deve ser alterada ao cancelar.             |
