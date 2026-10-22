## Cenário 30: Aplicação de fichas de anamnese.

### Caso de Teste 01: Aplicar nova anamnese a um aluno.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C30-CT01 | O sistema deve permitir aplicar uma ficha de anamnese.     |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O cliente e um modelo de anamnese ativo devem estar cadastrados. |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Fichas Anamnese"            |
| **E** clica em "Nova Anamnese"                                    |
| **E** seleciona o aluno "Hendreu Teste" e o modelo de anamnese    |
| **QUANDO** salvar a ficha                                         |
| **ENTÃO** a ficha deve ser exibida na lista com status "Pendente" ou "Concluído" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A ficha deve aparecer na lista para o aluno correto.            |

---

### Caso de Teste 02: Tentar aplicar anamnese sem selecionar aluno.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C30-CT02 | O sistema deve impedir a ficha sem aluno.                  |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Anamnese"              |
| **E** não seleciona nenhum aluno                                  |
| **QUANDO** salvar a ficha                                         |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A ficha não deve ser salva sem aluno.                           |

---

### Caso de Teste 03: Filtrar fichas por status.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C30-CT03 | O sistema deve listar apenas as fichas do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir fichas de anamnese aplicadas.                   |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Fichas Anamnese"            |
| **QUANDO** selecionar "Pendente" no filtro de status              |
| **ENTÃO** somente fichas pendentes devem ser exibidas             |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
