## Cenário 32: Gestão de categorias de anamnese.

### Caso de Teste 01: Adicionar nova categoria com dados válidos.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C32-CT01 | O sistema deve permitir o cadastro de uma categoria.       |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Categorias.  |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Categorias" da Anamnese     |
| **E** clica em "Nova Categoria"                                   |
| **E** preenche "Histórico de lesões" no Nome                      |
| **QUANDO** salvar a categoria                                     |
| **ENTÃO** a categoria deve ser exibida na lista com status "Ativo" |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A categoria deve aparecer corretamente na lista.                |

---

### Caso de Teste 02: Tentar adicionar categoria sem nome.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C32-CT02 | O sistema deve impedir o cadastro de categoria sem nome.   |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Categoria"             |
| **E** deixa o campo Nome em branco                                |
| **QUANDO** salvar a categoria                                     |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A categoria não deve ser salva sem nome.                        |

---

### Caso de Teste 03: Filtrar categorias por status.

| ID       | Descrição                                                         |
| :------- | :---------------------------------------------------------------- |
| C32-CT03 | O sistema deve listar apenas as categorias do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir categorias cadastradas.                         |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Categorias" da Anamnese     |
| **QUANDO** selecionar "Ativo" no filtro de status                 |
| **ENTÃO** somente categorias ativas devem ser exibidas            |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
