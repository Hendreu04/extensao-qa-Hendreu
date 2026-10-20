## Cenário 21: Gestão de despesas fixas.

### Caso de Teste 01: Adicionar nova despesa fixa com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C21-CT01 | O sistema deve permitir o cadastro de uma despesa fixa.    |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Despesas Fixas. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Despesas Fixas"             |
| **E** clica para cadastrar uma nova despesa                       |
| **E** preenche "Internet Hendreu", o valor "100,00" e a recorrência "1 Mês" |
| **QUANDO** salvar a despesa                                       |
| **ENTÃO** a despesa deve ser exibida na lista com status "ATIVO"  |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A despesa deve aparecer com o valor e a recorrência corretos.   |

---

### Caso de Teste 02: Filtrar despesas por recorrência.

| ID       | Descrição                                                            |
| :------- | :------------------------------------------------------------------- |
| C21-CT02 | O sistema deve listar apenas as despesas da recorrência selecionada. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir despesas com recorrências diferentes.           |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Despesas Fixas"             |
| **QUANDO** selecionar "1 Ano" no filtro Recorrência               |
| **ENTÃO** somente despesas com recorrência de 1 ano devem ser exibidas |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas a recorrência selecionada.          |

---

### Caso de Teste 03: Verificar valor total das despesas.

| ID       | Descrição                                                       |
| :------- | :-------------------------------------------------------------- |
| C21-CT03 | O card de valor deve corresponder à soma das despesas listadas. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir despesas cadastradas.                           |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Despesas Fixas"             |
| **QUANDO** comparar o card "Valor Listado" com a soma dos valores da lista |
| **ENTÃO** os valores devem ser iguais                             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O total exibido deve ser igual à soma das despesas.             |
