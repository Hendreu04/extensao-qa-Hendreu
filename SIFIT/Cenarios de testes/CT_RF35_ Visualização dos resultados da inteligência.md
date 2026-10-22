## Cenário 35: Visualização dos resultados da inteligência.

### Caso de Teste 01: Visualizar resultados da inteligência.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C35-CT01 | O sistema deve exibir os resultados das automações.        |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Resultados IA"              |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** os cards de resultados e o histórico devem ser exibidos |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A tela deve carregar corretamente.                              |

---

### Caso de Teste 02: Filtrar resultados por período.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C35-CT02 | O sistema deve atualizar os resultados conforme o período escolhido. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Resultados IA"              |
| **QUANDO** clicar em "Últimos 30 dias"                            |
| **ENTÃO** os cards e o histórico devem ser atualizados para o período |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os resultados devem corresponder ao período selecionado.        |

---

### Caso de Teste 03: Verificar quantidade de inadimplentes.

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C35-CT03 | O número de inadimplentes deve ser coerente com o restante do sistema. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Resultados IA"              |
| **QUANDO** comparar o card de alunos inadimplentes com o valor em aberto exibido na Página Inicial |
| **ENTÃO** as informações devem ser coerentes entre si             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os dados de inadimplência não devem se contradizer.             |
