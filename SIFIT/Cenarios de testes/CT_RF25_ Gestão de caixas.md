## Cenário 25: Gestão de caixas.

### Caso de Teste 01: Abrir caixa com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C25-CT01 | O sistema deve permitir a abertura de um caixa.            |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Caixas.      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Caixas"                     |
| **E** clica em "Abrir Caixa"                                      |
| **E** preenche os dados de abertura                               |
| **QUANDO** confirmar a abertura                                   |
| **ENTÃO** o caixa deve ser exibido na lista com status "ABERTO"   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O caixa deve aparecer na lista com a data de hoje.              |

---

### Caso de Teste 02: Filtrar caixas por status.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C25-CT02 | O sistema deve listar apenas os caixas do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir caixas abertos e fechados.                      |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Caixas"                     |
| **E** seleciona "Fechado" no filtro Status                        |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente caixas fechados devem ser exibidos              |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |

---

### Caso de Teste 03: Navegar entre as páginas da lista de caixas.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C25-CT03 | A paginação deve exibir os demais caixas.                  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir mais de 10 caixas cadastrados.                  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Caixas"                     |
| **QUANDO** clicar na página "2"                                   |
| **ENTÃO** os próximos caixas da lista devem ser exibidos          |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A paginação deve funcionar corretamente.                        |
