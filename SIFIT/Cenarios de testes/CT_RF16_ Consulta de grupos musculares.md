## Cenário 16: Consulta de grupos musculares.

### Caso de Teste 01: Visualizar lista de grupos musculares.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C16-CT01 | O sistema deve exibir os grupos musculares cadastrados.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos musculares cadastrados.                  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos Musculares"          |
| **QUANDO** a página for carregada                                 |
| **ENTÃO** a lista de grupos deve ser exibida com o nome e o tipo de membro |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os grupos devem ser exibidos corretamente.                      |

---

### Caso de Teste 02: Filtrar grupos por tipo de membro.

| ID       | Descrição                                                   |
| :------- | :---------------------------------------------------------- |
| C16-CT02 | O sistema deve listar apenas os grupos do tipo selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos de tipos diferentes.                     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos Musculares"          |
| **E** seleciona "Inferiores" no filtro Tipo Membro                |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente grupos do tipo "Inferiores" devem ser exibidos  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o tipo selecionado.                 |

---

### Caso de Teste 03: Verificar total de grupos cadastrados.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C16-CT03 | O card de total deve corresponder à soma dos grupos por tipo. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir grupos cadastrados.                             |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Grupos Musculares"          |
| **QUANDO** comparar o card "Grupos cadastrados" com a soma dos cards Superiores, Inferiores e Aeróbio |
| **ENTÃO** os valores devem ser iguais                             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Os totais exibidos devem ser coerentes.                         |
