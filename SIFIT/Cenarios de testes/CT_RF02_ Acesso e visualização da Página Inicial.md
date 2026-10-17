## Cenário 02: Acesso e visualização da Página Inicial.

### Caso de Teste 01: Acesso à Página Inicial após login bem-sucedido.

| ID       | Descrição                                                              |
| :------- | :--------------------------------------------------------------------- |
| C02-CT01 | Verificar a exibição correta da Página Inicial após login com sucesso. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar autenticado com credenciais válidas.     |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessou o sistema com sucesso              |
| **QUANDO** for redirecionado automaticamente após o login         |
| **ENTÃO** a Página Inicial deve ser exibida com a saudação e os cards de indicadores |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| O sistema deve exibir corretamente a Página Inicial.            |

---

### Caso de Teste 02: Atualizar a página em uma tela interna.

| ID       | Descrição                                                     |
| :------- | :------------------------------------------------------------ |
| C02-CT02 | O sistema deve recarregar a mesma tela ao atualizar a página. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar logado no sistema.                       |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário acessa o menu "Clientes"                   |
| **QUANDO** pressionar F5 para atualizar a página                  |
| **ENTÃO** a tela de Clientes deve ser carregada novamente         |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| A tela deve recarregar sem erro e sem perder o login.           |

---

### Caso de Teste 03: Navegação pelo menu lateral.

| ID       | Descrição                                                      |
| :------- | :------------------------------------------------------------- |
| C02-CT03 | Os itens do menu lateral devem abrir as telas correspondentes. |

| **Pré-condições**                                             |
| :------------------------------------------------------------ |
| O usuário deve estar na Página Inicial após login.            |

| **Passos**                                                        |
| :---------------------------------------------------------------- |
| **DADO** que o usuário está na Página Inicial                     |
| **QUANDO** clicar nos itens "Clientes", "Matrículas" e "Planos" do menu lateral |
| **ENTÃO** cada tela correspondente deve ser exibida               |

| **Critérios de aceitação**                                      |
| :-------------------------------------------------------------- |
| Todos os itens do menu devem abrir a tela correta.              |
