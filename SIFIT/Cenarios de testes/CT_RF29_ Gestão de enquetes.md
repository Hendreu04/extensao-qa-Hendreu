## Cenário 29: Gestão de enquetes.

### Caso de Teste 01: Adicionar nova enquete com pergunta.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C29-CT01 | O sistema deve permitir o cadastro de uma enquete.         |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado e ter acesso ao menu Enquetes.    |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Enquetes"                   |
| **E** clica em "Nova Enquete"                                     |
| **E** preenche "Enquete Hendreu" no Nome e cadastra uma pergunta  |
| **QUANDO** salvar a enquete                                       |
| **ENTÃO** a enquete deve ser exibida na lista com a pergunta cadastrada |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A enquete deve aparecer com a pergunta correta.                 |

---

### Caso de Teste 02: Tentar ativar enquete sem pergunta.

| ID       | Descrição                                                  |
| :------- | :--------------------------------------------------------- |
| C29-CT02 | O sistema deve impedir enquete ativa sem nenhuma pergunta. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa a tela "Nova Enquete"               |
| **E** preenche o Nome e marca o status "Ativo"                    |
| **E** não cadastra nenhuma pergunta                               |
| **QUANDO** salvar a enquete                                       |
| **ENTÃO** uma mensagem de erro deve ser exibida                   |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A enquete não deve ser ativada sem pergunta.                    |

---

### Caso de Teste 03: Filtrar enquetes por status.

| ID       | Descrição                                                       |
| :------- | :-------------------------------------------------------------- |
| C29-CT03 | O sistema deve listar apenas as enquetes do status selecionado. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| Devem existir enquetes ativas e inativas.                     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Enquetes"                   |
| **E** seleciona "Inativo" no filtro Status                        |
| **QUANDO** clicar em "Buscar"                                     |
| **ENTÃO** somente enquetes inativas devem ser exibidas            |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O filtro deve exibir apenas o status selecionado.               |
